# Utilities / bsn

Big Switch Networks

**Table of contents**
* [Show fabric operating mode](#show-fabric-operating-mode)

---

### Show fabric operating mode

```
bsnc-01s# show forwarding-mode
auto-select  mode-1       mode-2       mode-3       mode-4       mode-5       mode-6       mode-7
bsnc-01s# show forwarding-mode mode-7
Forwarding Mode                  : mode-7
Max Endpoint Count               : 46000
Max IPv4 Address Count           : 46000
Max IPv6 Address Count           : 0
Max IPv4 Subnet Count            : 6000
Max IPv6 Subnet Count            : 0
Max EVPC Tenant IPv4 Route Count : 10000
Max EVPC Tenant IPv6 Route Count : 0
Max System IPv4 Route Count      : 10000
Max System IPv6 Route Count      : 0
Max EVPC Tenant ACL Count        : 3000
Max System Router ACL Count      : 500
Max QoS Classifier Rule Count    : 0
Unsupported Features             : vlan mapping 'global', qos policy, bgpv6, ospfv3, ipv6
~~~~~ Supported Leaf Switches ~~~~~
#  Vendor Model      ASIC
--|------|----------|-------------|
1  accton as5710-54x trident2
2  accton as5712-54x trident2
3  accton as5812-54t trident2-plus
4  accton as5812-54x trident2-plus
5  accton as6700-32x trident2
6  accton as6712-32x trident2
7  accton as6812-32x trident2-plus
8  dell   s4048-on   trident2
9  dell   s4048t-on  trident2-plus
10 dell   s4112f-on  maverick
11 dell   s4112t-on  maverick
12 dell   s4148f-on  maverick
13 dell   s4148t-on  maverick
14 dell   s6000-on   trident2
15 dell   s6010-on   trident2-plus

~~~~ Supported Spine Switches  ~~~~
#  Vendor Model      ASIC
--|------|----------|-------------|
1  accton as5710-54x trident2
2  accton as5712-54x trident2
3  accton as5812-54t trident2-plus
4  accton as5812-54x trident2-plus
5  accton as6700-32x trident2
6  accton as6712-32x trident2
7  accton as6812-32x trident2-plus
8  accton as7712-32x tomahawk
9  dell   s4048-on   trident2
10 dell   s4048t-on  trident2-plus
11 dell   s4112f-on  maverick
12 dell   s4112t-on  maverick
13 dell   s4148f-on  maverick
14 dell   s4148t-on  maverick
15 dell   s5048f-on  tomahawk-plus
16 dell   s6000-on   trident2
17 dell   s6010-on   trident2-plus
18 dell   s6100-on   tomahawk
19 dell   z9100-on   tomahawk
```
