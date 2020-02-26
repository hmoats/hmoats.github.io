# Utilities / tcpdump

tcpdump

**Table of contents**
* [Save to file and rotate](#save-to-file-and-rotate)

---

### Save to file and rotate

```
tcpdump -nn -i eth0 -w /var/tmp/eth0-cap -W 40 -C 40 port 5432

# -nn           Do not convert IPs and ports to names (no DNS lookups)
# -c 40         rotate after 40MB
# -W 40         Keep only 40 captures and rotate files
```
