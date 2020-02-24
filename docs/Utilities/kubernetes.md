# Utilities / kubernetes

**Table of contents**
* [Running tcpdump for a POD on the worker node](#running-tcpdump-for-a-pod-on-the-worker-node)

---

### Running tcpdump for a POD on the worker node

Step 1: Find the container name and the node your app is running on
```
hmoats@ip-10-18-4-10:~$ kubectl get pod postgresql-adapter-service-3884708540-3r93q -o json | grep -e containerID -e hostIP
                "containerID": "docker://c45b4f362eb8c7448f0f4b86f463bxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
        "hostIP": "10.24.43.166",

```

Step 2: Then from the worker with the IP "10.24.43.166", find the pods unique network interface index inside it's container.
```
admin@ip-10-24-43-166:~$ sudo docker exec c45b4f362eb8c7448f0f4b86f463bxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx /bin/sh -c 'cat /sys/class/net/eth0/iflink'
271
```

Step 3: Then take the result from that and locate that interface on the worker
```
admin@ip-10-24-43-166:~$ ip link | grep 271
271: vethwepl490e39a@if270: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 8912 qdisc noqueue master weave state UP mode DEFAULT group default
```

Step 4: Run tcpdump on the interface
```
admin@ip-10-24-43-166:~$ sudo tcpdump -i vethwepl490e39a port 5432 -w out4.pcap
```
