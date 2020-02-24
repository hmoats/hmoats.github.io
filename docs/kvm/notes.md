# Removing VM from kvm host

virsh list --all
virsh shutdown <VM>
virsh undefine --domain <VM>
cd /opt/vm
rm <VM>.img

