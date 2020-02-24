# Big Switch / Cisco to BSN CLI

| Cisco | BSN | Caveats | 
|:--------------------------------------|:-------------------------------------|:-|
| `no equivalent`  | `debug bash` | Drops the user into the the Linux shell. |
| `show interface description` | `show running-config switch | grep -e switch -e interface -e description -e shutdown` | There seems to be no way to simply get an interface status and description from the available `show switch all interface` command. Here we simply use the running configuration to see what interfaces have a description configuration. |
| `show interface status` | `show switch all interface` | Show interface status but does not include descriptions. |
| `show tech`  | `support` | Creates a support bundle. |
| `no equivalent`  | `show fabric error` | Provides quick view of fabric errors |
| `no equivalent`  | `show fabric warnings` | Provides quick view of fabric warnings |
