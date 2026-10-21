### SPINE-A1
```
root@SPINE-A1> show configuration | display set
set version 24.2R1-S2.5
set system host-name SPINE-A1
set system root-authentication encrypted-password "$6$ZDfs5I8D$QA5w5mmf0c/7yscdKmYJWic3egUcFa.1cGL8aSQZsdF2CLkXfsQ/viWJnRFHvSZblE4HHvgYBa0o80UXBroiq/"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/1 unit 0 family inet address 172.16.11.0/31
set interfaces ge-0/0/2 unit 0 family inet address 172.16.12.0/31
set interfaces ge-0/0/9 unit 0 family inet address 100.1.1.1/31
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AD402D0EA
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AD402D0EA
set interfaces lo0 unit 0 family inet address 192.168.1.1/32
set policy-options prefix-list LOOPBACK-PREFIX-LIST 192.168.1.1/32
set policy-options policy-statement BGP-TO-L3VPN term 01_LOOPBACK from protocol direct
set policy-options policy-statement BGP-TO-L3VPN term 01_LOOPBACK from prefix-list LOOPBACK-PREFIX-LIST
set policy-options policy-statement BGP-TO-L3VPN term 01_LOOPBACK then community add ASS-DC
set policy-options policy-statement BGP-TO-L3VPN term 01_LOOPBACK then accept
set policy-options policy-statement BGP-TO-L3VPN term 02_BGP_MARK-DC from protocol bgp
set policy-options policy-statement BGP-TO-L3VPN term 02_BGP_MARK-DC then community add ASS-DC
set policy-options policy-statement BGP-TO-L3VPN term 02_BGP_MARK-DC then accept
set policy-options policy-statement L3VPN-to-BGP term 01_DENY-LOCAL-DC from community ASS-DC
set policy-options policy-statement L3VPN-to-BGP term 01_DENY-LOCAL-DC then reject
set policy-options policy-statement L3VPN-to-BGP term 10_PREFER-L3VPN from protocol bgp
set policy-options policy-statement L3VPN-to-BGP term 10_PREFER-L3VPN then local-preference 150
set policy-options policy-statement L3VPN-to-BGP term 10_PREFER-L3VPN then accept
set policy-options policy-statement LOAD-BALANCE-POLICY term 1 then load-balance per-flow
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 from interface lo0.0
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 then accept
set policy-options community ASS-DC members 65000:1234
set routing-options route-distinguisher-id 192.168.1.1
set routing-options router-id 192.168.1.1
set routing-options autonomous-system 65001
set routing-options forwarding-table export LOAD-BALANCE-POLICY
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group ISP-L3VPN type external
set protocols bgp group ISP-L3VPN import L3VPN-to-BGP
set protocols bgp group ISP-L3VPN export BGP-TO-L3VPN
set protocols bgp group ISP-L3VPN peer-as 64512
set protocols bgp group ISP-L3VPN neighbor 100.1.1.0 local-address 100.1.1.1
set protocols bgp group UNDERLAY type external
set protocols bgp group UNDERLAY export LOOPBACK-TO-BGP
set protocols bgp group UNDERLAY multipath multiple-as
set protocols bgp group UNDERLAY neighbor 172.16.11.1 peer-as 65003
set protocols bgp group UNDERLAY neighbor 172.16.12.1 peer-as 65004
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.1
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY multipath
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.2
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols bgp group OVERLAY neighbor 192.168.1.6
set protocols bgp group OVERLAY neighbor 192.168.1.7
set protocols bgp group OVERLAY neighbor 192.168.1.8
```
### SPINE-A2
```
root@SPINE-A2> show configuration | display set
set version 24.2R1-S2.5
set system host-name SPINE-A2
set system root-authentication encrypted-password "$6$ZDfs5I8D$QA5w5mmf0c/7yscdKmYJWic3egUcFa.1cGL8aSQZsdF2CLkXfsQ/viWJnRFHvSZblE4HHvgYBa0o80UXBroiq/"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/1 unit 0 family inet address 172.16.21.0/31
set interfaces ge-0/0/2 unit 0 family inet address 172.16.22.0/31
set interfaces ge-0/0/8 unit 0 family inet address 100.1.2.1/31
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AD4B90CD5
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AD4B90CD5
set interfaces lo0 unit 0 family inet address 192.168.1.2/32
set policy-options prefix-list LOOPBACK-PREFIX-LIST 192.168.1.2/32
set policy-options policy-statement BGP-TO-L3VPN term 01_LOOPBACK from protocol direct
set policy-options policy-statement BGP-TO-L3VPN term 01_LOOPBACK from prefix-list LOOPBACK-PREFIX-LIST
set policy-options policy-statement BGP-TO-L3VPN term 01_LOOPBACK then community add ASS-DC
set policy-options policy-statement BGP-TO-L3VPN term 01_LOOPBACK then accept
set policy-options policy-statement BGP-TO-L3VPN term 02_BGP_MARK-DC from protocol bgp
set policy-options policy-statement BGP-TO-L3VPN term 02_BGP_MARK-DC then community add ASS-DC
set policy-options policy-statement BGP-TO-L3VPN term 02_BGP_MARK-DC then accept
set policy-options policy-statement L3VPN-to-BGP term 01_DENY-LOCAL-DC from community ASS-DC
set policy-options policy-statement L3VPN-to-BGP term 01_DENY-LOCAL-DC then reject
set policy-options policy-statement LOAD-BALANCE-POLICY term 1 then load-balance per-flow
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 from interface lo0.0
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 then accept
set policy-options community ASS-DC members 65000:1234
set routing-options route-distinguisher-id 192.168.1.2
set routing-options router-id 192.168.1.2
set routing-options autonomous-system 65002
set routing-options forwarding-table export LOAD-BALANCE-POLICY
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group ISP-L3VPN type external
set protocols bgp group ISP-L3VPN import L3VPN-to-BGP
set protocols bgp group ISP-L3VPN export BGP-TO-L3VPN
set protocols bgp group ISP-L3VPN peer-as 64512
set protocols bgp group ISP-L3VPN neighbor 100.1.2.0 local-address 100.1.2.1
set protocols bgp group UNDERLAY type external
set protocols bgp group UNDERLAY export LOOPBACK-TO-BGP
set protocols bgp group UNDERLAY multipath multiple-as
set protocols bgp group UNDERLAY neighbor 172.16.21.1 peer-as 65003
set protocols bgp group UNDERLAY neighbor 172.16.22.1 peer-as 65004
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.2
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY multipath
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.1
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols bgp group OVERLAY neighbor 192.168.1.6
set protocols bgp group OVERLAY neighbor 192.168.1.7
set protocols bgp group OVERLAY neighbor 192.168.1.8
```
### LEAF-A1
```
root@LEAF-A1> show configuration | display set
set version 24.4R1.9
set system host-name LEAF-A1
set system root-authentication encrypted-password "$6$Xr569liX$TjNLMnIdXZJe8XOEXuQB8wNRisnpbyo9RDKMAppMlpt9QFux0IaeAuWp0gRC7GYbkxs.e3oZVrg8YJ7KChhk4/"
set system arp aging-timer 5
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set chassis aggregated-devices ethernet device-count 2
set interfaces ge-0/0/1 unit 0 family inet address 172.16.11.1/31
set interfaces ge-0/0/2 unit 0 family inet address 172.16.21.1/31
set interfaces ge-0/0/8 gigether-options 802.3ad ae1
set interfaces ge-0/0/9 gigether-options 802.3ad ae0
set interfaces ae0 flexible-vlan-tagging
set interfaces ae0 encapsulation flexible-ethernet-services
set interfaces ae0 esi 00:01:00:00:00:00:00:00:00:01
set interfaces ae0 esi all-active
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp system-id 00:00:00:00:00:01
set interfaces ae0 unit 10 encapsulation vlan-bridge
set interfaces ae0 unit 10 vlan-id 10
set interfaces ae1 flexible-vlan-tagging
set interfaces ae1 encapsulation flexible-ethernet-services
set interfaces ae1 esi 00:01:00:00:00:00:00:00:00:02
set interfaces ae1 esi all-active
set interfaces ae1 aggregated-ether-options lacp active
set interfaces ae1 aggregated-ether-options lacp system-id 00:00:00:00:00:02
set interfaces ae1 unit 20 encapsulation vlan-bridge
set interfaces ae1 unit 20 vlan-id 20
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-ex9214-VM6AD60C08D5
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:ex9214:VM6AD60C08D5
set interfaces irb unit 10 family inet address 10.100.10.253/24 virtual-gateway-address 10.100.10.254
set interfaces irb unit 20 family inet address 10.200.10.253/24 virtual-gateway-address 10.200.10.254
set interfaces lo0 unit 0 family inet address 192.168.1.3/32
set multi-chassis mc-lag consistency-check
set policy-options prefix-list LOOPBACK-PREFIX-LIST 192.168.1.3/32
set policy-options policy-statement LOAD-BALANCE-POLICY term 1 then load-balance per-flow
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 from interface lo0.0
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 then accept
set routing-instances GREEN-L3PVN-VRF instance-type vrf
set routing-instances GREEN-L3PVN-VRF protocols evpn ip-prefix-routes advertise direct-nexthop
set routing-instances GREEN-L3PVN-VRF protocols evpn ip-prefix-routes encapsulation vxlan
set routing-instances GREEN-L3PVN-VRF protocols evpn ip-prefix-routes vni 5200
set routing-instances GREEN-L3PVN-VRF interface irb.20
set routing-instances GREEN-L3PVN-VRF vrf-target target:65000:2000
set routing-instances GREEN-VLAN-BASED-EVI instance-type evpn
set routing-instances GREEN-VLAN-BASED-EVI protocols evpn encapsulation vxlan
set routing-instances GREEN-VLAN-BASED-EVI vtep-source-interface lo0.0
set routing-instances GREEN-VLAN-BASED-EVI vlan-id 20
set routing-instances GREEN-VLAN-BASED-EVI vxlan vni 5020
set routing-instances GREEN-VLAN-BASED-EVI l3-interface irb.20
set routing-instances GREEN-VLAN-BASED-EVI interface ae1.20
set routing-instances GREEN-VLAN-BASED-EVI vrf-target target:65000:200
set routing-instances RED-L3PVN-VRF instance-type vrf
set routing-instances RED-L3PVN-VRF protocols evpn ip-prefix-routes advertise direct-nexthop
set routing-instances RED-L3PVN-VRF protocols evpn ip-prefix-routes encapsulation vxlan
set routing-instances RED-L3PVN-VRF protocols evpn ip-prefix-routes vni 5100
set routing-instances RED-L3PVN-VRF interface irb.10
set routing-instances RED-L3PVN-VRF vrf-target target:65000:1000
set routing-instances RED-VLAN-BASED-EVI instance-type evpn
set routing-instances RED-VLAN-BASED-EVI protocols evpn encapsulation vxlan
set routing-instances RED-VLAN-BASED-EVI vtep-source-interface lo0.0
set routing-instances RED-VLAN-BASED-EVI vlan-id 10
set routing-instances RED-VLAN-BASED-EVI vxlan vni 5010
set routing-instances RED-VLAN-BASED-EVI l3-interface irb.10
set routing-instances RED-VLAN-BASED-EVI interface ae0.10
set routing-instances RED-VLAN-BASED-EVI vrf-target target:65000:100
set routing-options route-distinguisher-id 192.168.1.3
set routing-options router-id 192.168.1.3
set routing-options autonomous-system 65003
set routing-options forwarding-table export LOAD-BALANCE-POLICY
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group UNDERLAY type external
set protocols bgp group UNDERLAY export LOOPBACK-TO-BGP
set protocols bgp group UNDERLAY multipath multiple-as
set protocols bgp group UNDERLAY neighbor 172.16.11.0 peer-as 65001
set protocols bgp group UNDERLAY neighbor 172.16.21.0 peer-as 65002
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.3
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY multipath
set protocols bgp group OVERLAY neighbor 192.168.1.2
set protocols bgp group OVERLAY neighbor 192.168.1.1
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols bgp group OVERLAY neighbor 192.168.1.6
set protocols bgp group OVERLAY neighbor 192.168.1.7
set protocols bgp group OVERLAY neighbor 192.168.1.8
set protocols lldp interface all
set protocols lldp-med interface all
```
### LEAF-A2
```
root@LEAF-A2> show configuration | display set
set version 24.4R1.9
set system host-name LEAF-A2
set system root-authentication encrypted-password "$6$Xr569liX$TjNLMnIdXZJe8XOEXuQB8wNRisnpbyo9RDKMAppMlpt9QFux0IaeAuWp0gRC7GYbkxs.e3oZVrg8YJ7KChhk4/"
set system arp aging-timer 5
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set chassis aggregated-devices ethernet device-count 2
set interfaces ge-0/0/1 unit 0 family inet address 172.16.12.1/31
set interfaces ge-0/0/2 unit 0 family inet address 172.16.22.1/31
set interfaces ge-0/0/8 gigether-options 802.3ad ae1
set interfaces ge-0/0/9 gigether-options 802.3ad ae0
set interfaces ae0 flexible-vlan-tagging
set interfaces ae0 encapsulation flexible-ethernet-services
set interfaces ae0 esi 00:01:00:00:00:00:00:00:00:01
set interfaces ae0 esi all-active
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp system-id 00:00:00:00:00:01
set interfaces ae0 unit 10 encapsulation vlan-bridge
set interfaces ae0 unit 10 vlan-id 10
set interfaces ae1 flexible-vlan-tagging
set interfaces ae1 encapsulation flexible-ethernet-services
set interfaces ae1 esi 00:01:00:00:00:00:00:00:00:02
set interfaces ae1 esi all-active
set interfaces ae1 aggregated-ether-options lacp active
set interfaces ae1 aggregated-ether-options lacp system-id 00:00:00:00:00:02
set interfaces ae1 unit 20 encapsulation vlan-bridge
set interfaces ae1 unit 20 vlan-id 20
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-ex9214-VM6AD60BC64F
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:ex9214:VM6AD60BC64F
set interfaces irb unit 10 family inet address 10.100.10.252/24 virtual-gateway-address 10.100.10.254
set interfaces irb unit 20 family inet address 10.200.10.252/24 virtual-gateway-address 10.200.10.254
set interfaces lo0 unit 0 family inet address 192.168.1.4/32
set multi-chassis mc-lag consistency-check
set policy-options prefix-list LOOPBACK-PREFIX-LIST 192.168.1.4/32
set policy-options policy-statement LOAD-BALANCE-POLICY term 1 then load-balance per-flow
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 from interface lo0.0
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 then accept
set routing-instances GREEN-L3PVN-VRF instance-type vrf
set routing-instances GREEN-L3PVN-VRF protocols evpn ip-prefix-routes advertise direct-nexthop
set routing-instances GREEN-L3PVN-VRF protocols evpn ip-prefix-routes encapsulation vxlan
set routing-instances GREEN-L3PVN-VRF protocols evpn ip-prefix-routes vni 5200
set routing-instances GREEN-L3PVN-VRF interface irb.20
set routing-instances GREEN-L3PVN-VRF vrf-target target:65000:2000
set routing-instances GREEN-VLAN-BASED-EVI instance-type evpn
set routing-instances GREEN-VLAN-BASED-EVI protocols evpn encapsulation vxlan
set routing-instances GREEN-VLAN-BASED-EVI vtep-source-interface lo0.0
set routing-instances GREEN-VLAN-BASED-EVI vlan-id 20
set routing-instances GREEN-VLAN-BASED-EVI vxlan vni 5020
set routing-instances GREEN-VLAN-BASED-EVI l3-interface irb.20
set routing-instances GREEN-VLAN-BASED-EVI interface ae1.20
set routing-instances GREEN-VLAN-BASED-EVI vrf-target target:65000:200
set routing-instances RED-L3PVN-VRF instance-type vrf
set routing-instances RED-L3PVN-VRF protocols evpn ip-prefix-routes advertise direct-nexthop
set routing-instances RED-L3PVN-VRF protocols evpn ip-prefix-routes encapsulation vxlan
set routing-instances RED-L3PVN-VRF protocols evpn ip-prefix-routes vni 5100
set routing-instances RED-L3PVN-VRF interface irb.10
set routing-instances RED-L3PVN-VRF vrf-target target:65000:1000
set routing-instances RED-VLAN-BASED-EVI instance-type evpn
set routing-instances RED-VLAN-BASED-EVI protocols evpn encapsulation vxlan
set routing-instances RED-VLAN-BASED-EVI vtep-source-interface lo0.0
set routing-instances RED-VLAN-BASED-EVI vlan-id 10
set routing-instances RED-VLAN-BASED-EVI vxlan vni 5010
set routing-instances RED-VLAN-BASED-EVI l3-interface irb.10
set routing-instances RED-VLAN-BASED-EVI interface ae0.10
set routing-instances RED-VLAN-BASED-EVI vrf-target target:65000:100
set routing-options route-distinguisher-id 192.168.1.4
set routing-options router-id 192.168.1.4
set routing-options autonomous-system 65004
set routing-options forwarding-table export LOAD-BALANCE-POLICY
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group UNDERLAY type external
set protocols bgp group UNDERLAY export LOOPBACK-TO-BGP
set protocols bgp group UNDERLAY multipath multiple-as
set protocols bgp group UNDERLAY neighbor 172.16.12.0 peer-as 65001
set protocols bgp group UNDERLAY neighbor 172.16.22.0 peer-as 65002
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.4
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY multipath
set protocols bgp group OVERLAY neighbor 192.168.1.2
set protocols bgp group OVERLAY neighbor 192.168.1.1
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols bgp group OVERLAY neighbor 192.168.1.6
set protocols bgp group OVERLAY neighbor 192.168.1.7
set protocols bgp group OVERLAY neighbor 192.168.1.8
set protocols lldp interface all
set protocols lldp-med interface all
```

### SPINE-B1
```
root@SPINE-B1> show configuration | display set
set version 24.2R1-S2.5
set system host-name SPINE-B1
set system root-authentication encrypted-password "$6$ZDfs5I8D$QA5w5mmf0c/7yscdKmYJWic3egUcFa.1cGL8aSQZsdF2CLkXfsQ/viWJnRFHvSZblE4HHvgYBa0o80UXBroiq/"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/1 unit 0 family inet address 172.16.31.0/31
set interfaces ge-0/0/2 unit 0 family inet address 172.16.32.0/31
set interfaces ge-0/0/9 unit 0 family inet address 100.2.1.1/31
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AD402D201
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AD402D201
set interfaces lo0 unit 0 family inet address 192.168.1.5/32
set policy-options prefix-list LOOPBACK-PREFIX-LIST 192.168.1.5/32
set policy-options policy-statement BGP-TO-L3VPN term 01_LOOPBACK from protocol direct
set policy-options policy-statement BGP-TO-L3VPN term 01_LOOPBACK from prefix-list LOOPBACK-PREFIX-LIST
set policy-options policy-statement BGP-TO-L3VPN term 01_LOOPBACK then community add BALLS-DC
set policy-options policy-statement BGP-TO-L3VPN term 01_LOOPBACK then accept
set policy-options policy-statement BGP-TO-L3VPN term 02_BGP_MARK-DC from protocol bgp
set policy-options policy-statement BGP-TO-L3VPN term 02_BGP_MARK-DC then community add BALLS-DC
set policy-options policy-statement BGP-TO-L3VPN term 02_BGP_MARK-DC then accept
set policy-options policy-statement L3VPN-to-BGP term 01_DENY-LOCAL-DC from community BALLS-DC
set policy-options policy-statement L3VPN-to-BGP term 01_DENY-LOCAL-DC then reject
set policy-options policy-statement L3VPN-to-BGP term 10_PREFER-L3VPN from protocol bgp
set policy-options policy-statement L3VPN-to-BGP term 10_PREFER-L3VPN then local-preference 150
set policy-options policy-statement L3VPN-to-BGP term 10_PREFER-L3VPN then accept
set policy-options policy-statement LOAD-BALANCE-POLICY term 1 then load-balance per-flow
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 from interface lo0.0
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 then accept
set policy-options community BALLS-DC members 65000:5678
set routing-options route-distinguisher-id 192.168.1.5
set routing-options router-id 192.168.1.5
set routing-options autonomous-system 65005
set routing-options forwarding-table export LOAD-BALANCE-POLICY
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group ISP-L3VPN type external
set protocols bgp group ISP-L3VPN hold-time 12
set protocols bgp group ISP-L3VPN import L3VPN-to-BGP
set protocols bgp group ISP-L3VPN export BGP-TO-L3VPN
set protocols bgp group ISP-L3VPN peer-as 64512
set protocols bgp group ISP-L3VPN bfd-liveness-detection minimum-interval 300
set protocols bgp group ISP-L3VPN bfd-liveness-detection multiplier 3
set protocols bgp group ISP-L3VPN neighbor 100.2.1.0 local-address 100.2.1.1
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.5
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY multipath
set protocols bgp group OVERLAY neighbor 192.168.1.1
set protocols bgp group OVERLAY neighbor 192.168.1.2
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.6
set protocols bgp group OVERLAY neighbor 192.168.1.7
set protocols bgp group OVERLAY neighbor 192.168.1.8
set protocols bgp group UNDERLAY type external
set protocols bgp group UNDERLAY hold-time 12
set protocols bgp group UNDERLAY export LOOPBACK-TO-BGP
set protocols bgp group UNDERLAY local-as 65005
set protocols bgp group UNDERLAY multipath multiple-as
set protocols bgp group UNDERLAY bfd-liveness-detection minimum-interval 300
set protocols bgp group UNDERLAY bfd-liveness-detection multiplier 3
set protocols bgp group UNDERLAY neighbor 172.16.31.1 peer-as 65007
set protocols bgp group UNDERLAY neighbor 172.16.32.1 peer-as 65008
```
### SPINE-B2
```
root@SPINE-B2> show configuration | display set
set version 24.2R1-S2.5
set system host-name SPINE-B2
set system root-authentication encrypted-password "$6$Xr569liX$TjNLMnIdXZJe8XOEXuQB8wNRisnpbyo9RDKMAppMlpt9QFux0IaeAuWp0gRC7GYbkxs.e3oZVrg8YJ7KChhk4/"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/1 unit 0 family inet address 172.16.41.0/31
set interfaces ge-0/0/2 unit 0 family inet address 172.16.42.0/31
set interfaces ge-0/0/8 unit 0 family inet address 100.2.2.1/31
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AD5CD0C7C
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AD5CD0C7C
set interfaces lo0 unit 0 family inet address 192.168.1.6/32
set policy-options prefix-list LOOPBACK-PREFIX-LIST 192.168.1.6/32
set policy-options policy-statement BGP-TO-L3VPN term 01_LOOPBACK from protocol direct
set policy-options policy-statement BGP-TO-L3VPN term 01_LOOPBACK from prefix-list LOOPBACK-PREFIX-LIST
set policy-options policy-statement BGP-TO-L3VPN term 01_LOOPBACK then community add BALLS-DC
set policy-options policy-statement BGP-TO-L3VPN term 01_LOOPBACK then accept
set policy-options policy-statement BGP-TO-L3VPN term 02_BGP_MARK-DC from protocol bgp
set policy-options policy-statement BGP-TO-L3VPN term 02_BGP_MARK-DC then community add BALLS-DC
set policy-options policy-statement BGP-TO-L3VPN term 02_BGP_MARK-DC then accept
set policy-options policy-statement L3VPN-to-BGP term 01_DENY-LOCAL-DC from community BALLS-DC
set policy-options policy-statement L3VPN-to-BGP term 01_DENY-LOCAL-DC then reject
set policy-options policy-statement L3VPN-to-BGP term 10_PREFER-L3VPN from protocol bgp
set policy-options policy-statement L3VPN-to-BGP term 10_PREFER-L3VPN then local-preference 150
set policy-options policy-statement L3VPN-to-BGP term 10_PREFER-L3VPN then accept
set policy-options policy-statement LOAD-BALANCE-POLICY term 1 then load-balance per-flow
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 from interface lo0.0
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 then accept
set policy-options community BALLS-DC members 65000:5678
set routing-options route-distinguisher-id 192.168.1.6
set routing-options router-id 192.168.1.6
set routing-options autonomous-system 65006
set routing-options forwarding-table export LOAD-BALANCE-POLICY
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group ISP-L3VPN type external
set protocols bgp group ISP-L3VPN hold-time 12
set protocols bgp group ISP-L3VPN import L3VPN-to-BGP
set protocols bgp group ISP-L3VPN export BGP-TO-L3VPN
set protocols bgp group ISP-L3VPN peer-as 64512
set protocols bgp group ISP-L3VPN bfd-liveness-detection minimum-interval 300
set protocols bgp group ISP-L3VPN bfd-liveness-detection multiplier 3
set protocols bgp group ISP-L3VPN neighbor 100.2.2.0 local-address 100.2.2.1
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.6
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY multipath
set protocols bgp group OVERLAY neighbor 192.168.1.1
set protocols bgp group OVERLAY neighbor 192.168.1.2
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols bgp group OVERLAY neighbor 192.168.1.7
set protocols bgp group OVERLAY neighbor 192.168.1.8
set protocols bgp group UNDERLAY type external
set protocols bgp group UNDERLAY hold-time 12
set protocols bgp group UNDERLAY export LOOPBACK-TO-BGP
set protocols bgp group UNDERLAY local-as 65006
set protocols bgp group UNDERLAY multipath multiple-as
set protocols bgp group UNDERLAY bfd-liveness-detection minimum-interval 300
set protocols bgp group UNDERLAY bfd-liveness-detection multiplier 3
set protocols bgp group UNDERLAY neighbor 172.16.41.1 peer-as 65007
set protocols bgp group UNDERLAY neighbor 172.16.42.1 peer-as 65008
```
### LEAF-B1
```
root@LEAF-B1> show configuration | display set
set version 24.4R1.9
set system host-name LEAF-B1
set system root-authentication encrypted-password "$6$2zSP0OoN$Tt1X1frNx1jETp6cD3nh3ubkwfLCb0PhP8wnrn5.aFYA3JpXjFVo.5iNONMFCzlS33Z47XI0vttDJJN2OU7D40"
set system arp aging-timer 5
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set chassis aggregated-devices ethernet device-count 2
set interfaces ge-0/0/1 unit 0 family inet address 172.16.31.1/31
set interfaces ge-0/0/2 unit 0 family inet address 172.16.41.1/31
set interfaces ge-0/0/8 gigether-options 802.3ad ae1
set interfaces ge-0/0/9 gigether-options 802.3ad ae0
set interfaces ae0 flexible-vlan-tagging
set interfaces ae0 encapsulation flexible-ethernet-services
set interfaces ae0 esi 00:02:00:00:00:00:00:00:00:01
set interfaces ae0 esi all-active
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp system-id 00:00:00:00:00:01
set interfaces ae0 unit 10 encapsulation vlan-bridge
set interfaces ae0 unit 10 vlan-id 10
set interfaces ae1 flexible-vlan-tagging
set interfaces ae1 encapsulation flexible-ethernet-services
set interfaces ae1 esi 00:02:00:00:00:00:00:00:00:02
set interfaces ae1 esi all-active
set interfaces ae1 aggregated-ether-options lacp active
set interfaces ae1 aggregated-ether-options lacp system-id 00:00:00:00:00:02
set interfaces ae1 unit 20 encapsulation vlan-bridge
set interfaces ae1 unit 20 vlan-id 20
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-ex9214-VM6AD72641D2
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:ex9214:VM6AD72641D2
set interfaces irb unit 10 family inet address 10.100.20.253/24 virtual-gateway-address 10.100.20.254
set interfaces irb unit 20 family inet address 10.200.20.253/24 virtual-gateway-address 10.200.20.254
set interfaces lo0 unit 0 family inet address 192.168.1.7/32
set multi-chassis mc-lag consistency-check
set policy-options prefix-list LOOPBACK-PREFIX-LIST 192.168.1.7/32
set policy-options policy-statement LOAD-BALANCE-POLICY term 1 then load-balance per-flow
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 from interface lo0.0
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 then accept
set routing-instances GREEN-L3PVN-VRF instance-type vrf
set routing-instances GREEN-L3PVN-VRF protocols evpn ip-prefix-routes advertise direct-nexthop
set routing-instances GREEN-L3PVN-VRF protocols evpn ip-prefix-routes encapsulation vxlan
set routing-instances GREEN-L3PVN-VRF protocols evpn ip-prefix-routes vni 5200
set routing-instances GREEN-L3PVN-VRF interface irb.20
set routing-instances GREEN-L3PVN-VRF vrf-target target:65000:2000
set routing-instances GREEN-VLAN-BASED-EVI instance-type evpn
set routing-instances GREEN-VLAN-BASED-EVI protocols evpn encapsulation vxlan
set routing-instances GREEN-VLAN-BASED-EVI vtep-source-interface lo0.0
set routing-instances GREEN-VLAN-BASED-EVI vlan-id 20
set routing-instances GREEN-VLAN-BASED-EVI vxlan vni 5021
set routing-instances GREEN-VLAN-BASED-EVI l3-interface irb.20
set routing-instances GREEN-VLAN-BASED-EVI interface ae1.20
set routing-instances GREEN-VLAN-BASED-EVI vrf-target target:65000:200
set routing-instances RED-L3PVN-VRF instance-type vrf
set routing-instances RED-L3PVN-VRF protocols evpn ip-prefix-routes advertise direct-nexthop
set routing-instances RED-L3PVN-VRF protocols evpn ip-prefix-routes encapsulation vxlan
set routing-instances RED-L3PVN-VRF protocols evpn ip-prefix-routes vni 5100
set routing-instances RED-L3PVN-VRF interface irb.10
set routing-instances RED-L3PVN-VRF vrf-target target:65000:1000
set routing-instances RED-VLAN-BASED-EVI instance-type evpn
set routing-instances RED-VLAN-BASED-EVI protocols evpn encapsulation vxlan
set routing-instances RED-VLAN-BASED-EVI vtep-source-interface lo0.0
set routing-instances RED-VLAN-BASED-EVI vlan-id 10
set routing-instances RED-VLAN-BASED-EVI vxlan vni 5011
set routing-instances RED-VLAN-BASED-EVI l3-interface irb.10
set routing-instances RED-VLAN-BASED-EVI interface ae0.10
set routing-instances RED-VLAN-BASED-EVI vrf-target target:65000:100
set routing-options route-distinguisher-id 192.168.1.7
set routing-options router-id 192.168.1.7
set routing-options autonomous-system 65007
set routing-options forwarding-table export LOAD-BALANCE-POLICY
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group UNDERLAY type external
set protocols bgp group UNDERLAY hold-time 12
set protocols bgp group UNDERLAY export LOOPBACK-TO-BGP
set protocols bgp group UNDERLAY local-as 65007
set protocols bgp group UNDERLAY multipath multiple-as
set protocols bgp group UNDERLAY bfd-liveness-detection minimum-interval 300
set protocols bgp group UNDERLAY bfd-liveness-detection multiplier 3
set protocols bgp group UNDERLAY neighbor 172.16.31.0 peer-as 65005
set protocols bgp group UNDERLAY neighbor 172.16.41.0 peer-as 65006
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.7
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY multipath
set protocols bgp group OVERLAY neighbor 192.168.1.1
set protocols bgp group OVERLAY neighbor 192.168.1.2
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols bgp group OVERLAY neighbor 192.168.1.6
set protocols bgp group OVERLAY neighbor 192.168.1.8
set protocols lldp interface all
set protocols lldp-med interface all
```
### LEAF-B2
```
root@LEAF-B2> show configuration | display set
set version 24.4R1.9
set system host-name LEAF-B2
set system root-authentication encrypted-password "$6$RyjMvk9H$Gs3kpFmqKv/kOOpfMJkKofnWxSIhD0DS9Vyl02UqadtiYPime1Tpl7cS.sT4gsCEuMeNaP73HGZtVe0TiOtmK0"
set system arp aging-timer 5
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set chassis aggregated-devices ethernet device-count 2
set interfaces ge-0/0/1 unit 0 family inet address 172.16.32.1/31
set interfaces ge-0/0/2 unit 0 family inet address 172.16.42.1/31
set interfaces ge-0/0/8 gigether-options 802.3ad ae1
set interfaces ge-0/0/9 gigether-options 802.3ad ae0
set interfaces ae0 flexible-vlan-tagging
set interfaces ae0 encapsulation flexible-ethernet-services
set interfaces ae0 esi 00:02:00:00:00:00:00:00:00:01
set interfaces ae0 esi all-active
set interfaces ae0 aggregated-ether-options lacp active
set interfaces ae0 aggregated-ether-options lacp system-id 00:00:00:00:00:01
set interfaces ae0 unit 10 encapsulation vlan-bridge
set interfaces ae0 unit 10 vlan-id 10
set interfaces ae1 flexible-vlan-tagging
set interfaces ae1 encapsulation flexible-ethernet-services
set interfaces ae1 esi 00:02:00:00:00:00:00:00:00:02
set interfaces ae1 esi all-active
set interfaces ae1 aggregated-ether-options lacp active
set interfaces ae1 aggregated-ether-options lacp system-id 00:00:00:00:00:02
set interfaces ae1 unit 20 encapsulation vlan-bridge
set interfaces ae1 unit 20 vlan-id 20
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-ex9214-VM6AD7264D5F
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:ex9214:VM6AD7264D5F
set interfaces irb unit 10 family inet address 10.100.20.252/24 virtual-gateway-address 10.100.20.254
set interfaces irb unit 20 family inet address 10.200.20.252/24 virtual-gateway-address 10.200.20.254
set interfaces lo0 unit 0 family inet address 192.168.1.8/32
set multi-chassis mc-lag consistency-check
set policy-options prefix-list LOOPBACK-PREFIX-LIST 192.168.1.8/32
set policy-options policy-statement LOAD-BALANCE-POLICY term 1 then load-balance per-flow
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 from interface lo0.0
set policy-options policy-statement LOOPBACK-TO-BGP term LOOPBACK-0 then accept
set routing-instances GREEN-L3PVN-VRF instance-type vrf
set routing-instances GREEN-L3PVN-VRF protocols evpn ip-prefix-routes advertise direct-nexthop
set routing-instances GREEN-L3PVN-VRF protocols evpn ip-prefix-routes encapsulation vxlan
set routing-instances GREEN-L3PVN-VRF protocols evpn ip-prefix-routes vni 5200
set routing-instances GREEN-L3PVN-VRF interface irb.20
set routing-instances GREEN-L3PVN-VRF vrf-target target:65000:2000
set routing-instances GREEN-VLAN-BASED-EVI instance-type evpn
set routing-instances GREEN-VLAN-BASED-EVI protocols evpn encapsulation vxlan
set routing-instances GREEN-VLAN-BASED-EVI vtep-source-interface lo0.0
set routing-instances GREEN-VLAN-BASED-EVI vlan-id 20
set routing-instances GREEN-VLAN-BASED-EVI vxlan vni 5021
set routing-instances GREEN-VLAN-BASED-EVI l3-interface irb.20
set routing-instances GREEN-VLAN-BASED-EVI interface ae1.20
set routing-instances GREEN-VLAN-BASED-EVI vrf-target target:65000:200
set routing-instances RED-L3PVN-VRF instance-type vrf
set routing-instances RED-L3PVN-VRF protocols evpn ip-prefix-routes advertise direct-nexthop
set routing-instances RED-L3PVN-VRF protocols evpn ip-prefix-routes encapsulation vxlan
set routing-instances RED-L3PVN-VRF protocols evpn ip-prefix-routes vni 5100
set routing-instances RED-L3PVN-VRF interface irb.10
set routing-instances RED-L3PVN-VRF vrf-target target:65000:1000
set routing-instances RED-VLAN-BASED-EVI instance-type evpn
set routing-instances RED-VLAN-BASED-EVI protocols evpn encapsulation vxlan
set routing-instances RED-VLAN-BASED-EVI vtep-source-interface lo0.0
set routing-instances RED-VLAN-BASED-EVI vlan-id 10
set routing-instances RED-VLAN-BASED-EVI vxlan vni 5011
set routing-instances RED-VLAN-BASED-EVI l3-interface irb.10
set routing-instances RED-VLAN-BASED-EVI interface ae0.10
set routing-instances RED-VLAN-BASED-EVI vrf-target target:65000:100
set routing-options route-distinguisher-id 192.168.1.8
set routing-options router-id 192.168.1.8
set routing-options autonomous-system 65008
set routing-options forwarding-table export LOAD-BALANCE-POLICY
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group OVERLAY type internal
set protocols bgp group OVERLAY local-address 192.168.1.8
set protocols bgp group OVERLAY family evpn signaling
set protocols bgp group OVERLAY local-as 65500
set protocols bgp group OVERLAY multipath
set protocols bgp group OVERLAY neighbor 192.168.1.1
set protocols bgp group OVERLAY neighbor 192.168.1.2
set protocols bgp group OVERLAY neighbor 192.168.1.4
set protocols bgp group OVERLAY neighbor 192.168.1.3
set protocols bgp group OVERLAY neighbor 192.168.1.5
set protocols bgp group OVERLAY neighbor 192.168.1.6
set protocols bgp group OVERLAY neighbor 192.168.1.7
set protocols bgp group UNDERLAY type external
set protocols bgp group UNDERLAY hold-time 12
set protocols bgp group UNDERLAY export LOOPBACK-TO-BGP
set protocols bgp group UNDERLAY local-as 65008
set protocols bgp group UNDERLAY multipath multiple-as
set protocols bgp group UNDERLAY bfd-liveness-detection minimum-interval 300
set protocols bgp group UNDERLAY bfd-liveness-detection multiplier 3
set protocols bgp group UNDERLAY neighbor 172.16.32.0 peer-as 65005
set protocols bgp group UNDERLAY neighbor 172.16.42.0 peer-as 65006
set protocols lldp interface all
set protocols lldp-med interface all
```

### PE1
```
root@PE1> show configuration | display set
set version 24.2R1-S2.5
set system host-name PE1
set system root-authentication encrypted-password "$6$ZDfs5I8D$QA5w5mmf0c/7yscdKmYJWic3egUcFa.1cGL8aSQZsdF2CLkXfsQ/viWJnRFHvSZblE4HHvgYBa0o80UXBroiq/"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/1 unit 0 family inet address 100.0.1.1/31
set interfaces ge-0/0/1 unit 0 family mpls
set interfaces ge-0/0/8 unit 0 family inet address 100.1.2.0/31
set interfaces ge-0/0/9 unit 0 family inet address 100.1.1.0/31
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AD4018C06
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AD4018C06
set interfaces lo0 unit 0 family inet address 192.168.255.1/32
set interfaces lo0 unit 0 family mpls
set policy-options policy-statement DC-LLC_EXPORT term 01_ACCEPT_BGP from protocol bgp
set policy-options policy-statement DC-LLC_EXPORT term 01_ACCEPT_BGP then community add DC-LLC_ALL-SITES
set policy-options policy-statement DC-LLC_EXPORT term 01_ACCEPT_BGP then accept
set policy-options policy-statement DC-LLC_EXPORT term 999_DROP_ANY then reject
set policy-options policy-statement DC-LLC_IMPORT term 01_ACCEPT_BGP from protocol bgp
set policy-options policy-statement DC-LLC_IMPORT term 01_ACCEPT_BGP from community DC-LLC_ALL-SITES
set policy-options policy-statement DC-LLC_IMPORT term 01_ACCEPT_BGP then accept
set policy-options policy-statement DC-LLC_IMPORT term 999_DROP_ANY then reject
set policy-options community DC-LLC_ALL-SITES members target:64512:101
set routing-instances DC-LLC_VRF instance-type vrf
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_VRF_65001 type external
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_VRF_65001 peer-as 65001
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_VRF_65001 neighbor 100.1.1.1 local-address 100.1.1.0
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_VRF_65001 neighbor 100.1.1.1 family inet unicast
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_VRF_65002 type external
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_VRF_65002 peer-as 65002
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_VRF_65002 neighbor 100.1.2.1 local-address 100.1.2.0
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_VRF_65002 neighbor 100.1.2.1 family inet unicast
set routing-instances DC-LLC_VRF interface ge-0/0/8.0
set routing-instances DC-LLC_VRF interface ge-0/0/9.0
set routing-instances DC-LLC_VRF vrf-import DC-LLC_IMPORT
set routing-instances DC-LLC_VRF vrf-export DC-LLC_EXPORT
set routing-instances DC-LLC_VRF vrf-target target:64512:101
set routing-options route-distinguisher-id 192.168.255.1
set routing-options router-id 192.168.255.1
set routing-options autonomous-system 64512
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group ISP-CORE type internal
set protocols bgp group ISP-CORE local-address 192.168.255.1
set protocols bgp group ISP-CORE family inet-vpn unicast
set protocols bgp group ISP-CORE neighbor 192.168.255.2
set protocols bgp group ISP-CORE neighbor 192.168.255.3
set protocols ldp interface ge-0/0/1.0
set protocols ldp interface lo0.0
set protocols mpls interface ge-0/0/1.0
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface lo0.0 passive
set protocols ospf reference-bandwidth 100g
```
### P1
```
root@P1> show configuration | display set
set version 24.2R1-S2.5
set system host-name P1
set system root-authentication encrypted-password "$6$ZDfs5I8D$QA5w5mmf0c/7yscdKmYJWic3egUcFa.1cGL8aSQZsdF2CLkXfsQ/viWJnRFHvSZblE4HHvgYBa0o80UXBroiq/"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/0 unit 0 family inet address 100.0.1.0/31
set interfaces ge-0/0/0 unit 0 family mpls
set interfaces ge-0/0/1 unit 0 family inet address 100.0.2.0/31
set interfaces ge-0/0/1 unit 0 family mpls
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AD4018E1B
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AD4018E1B
set interfaces lo0 unit 0 family inet address 192.168.255.2/32
set interfaces lo0 unit 0 family mpls
set routing-options route-distinguisher-id 192.168.255.2
set routing-options router-id 192.168.255.2
set routing-options autonomous-system 64512
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group ISP-CORE type internal
set protocols bgp group ISP-CORE local-address 192.168.255.2
set protocols bgp group ISP-CORE family inet-vpn unicast
set protocols bgp group ISP-CORE neighbor 192.168.255.1
set protocols bgp group ISP-CORE neighbor 192.168.255.3
set protocols ldp interface ge-0/0/0.0
set protocols ldp interface ge-0/0/1.0
set protocols ldp interface lo0.0
set protocols mpls interface ge-0/0/1.0
set protocols mpls interface ge-0/0/0.0
set protocols ospf area 0.0.0.0 interface ge-0/0/0.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface lo0.0 passive
set protocols ospf reference-bandwidth 100g
```
### PE2
```
root@PE2> show configuration | display set
set version 24.2R1-S2.5
set system host-name PE2
set system root-authentication encrypted-password "$6$ZDfs5I8D$QA5w5mmf0c/7yscdKmYJWic3egUcFa.1cGL8aSQZsdF2CLkXfsQ/viWJnRFHvSZblE4HHvgYBa0o80UXBroiq/"
set system syslog file interactive-commands interactive-commands any
set system syslog file messages any notice
set system syslog file messages authorization info
set system processes dhcp-service traceoptions file dhcp_logfile
set system processes dhcp-service traceoptions file size 10m
set system processes dhcp-service traceoptions level all
set system processes dhcp-service traceoptions flag packet
set interfaces ge-0/0/1 unit 0 family inet address 100.0.2.1/31
set interfaces ge-0/0/1 unit 0 family mpls
set interfaces ge-0/0/8 unit 0 family inet address 100.2.2.0/31
set interfaces ge-0/0/9 unit 0 family inet address 100.2.1.0/31
set interfaces fxp0 unit 0 family inet dhcp vendor-id Juniper-vmx-VM6AD4018F84
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-type stateful
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-ia-type ia-na
set interfaces fxp0 unit 0 family inet6 dhcpv6-client client-identifier duid-type duid-ll
set interfaces fxp0 unit 0 family inet6 dhcpv6-client vendor-id Juniper:vmx:VM6AD4018F84
set interfaces lo0 unit 0 family inet address 192.168.255.3/32
set interfaces lo0 unit 0 family mpls
set policy-options policy-statement DC-LLC_EXPORT term 01_ACCEPT_BGP from protocol bgp
set policy-options policy-statement DC-LLC_EXPORT term 01_ACCEPT_BGP then community add DC-LLC_ALL-SITES
set policy-options policy-statement DC-LLC_EXPORT term 01_ACCEPT_BGP then accept
set policy-options policy-statement DC-LLC_EXPORT term 999_DROP_ANY then reject
set policy-options policy-statement DC-LLC_IMPORT term 01_ACCEPT_BGP from protocol bgp
set policy-options policy-statement DC-LLC_IMPORT term 01_ACCEPT_BGP from community DC-LLC_ALL-SITES
set policy-options policy-statement DC-LLC_IMPORT term 01_ACCEPT_BGP then accept
set policy-options policy-statement DC-LLC_IMPORT term 999_DROP_ANY then reject
set policy-options community DC-LLC_ALL-SITES members target:64512:101
set routing-instances DC-LLC_VRF instance-type vrf
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_65005 type external
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_65005 hold-time 12
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_65005 peer-as 65005
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_65005 bfd-liveness-detection minimum-interval 300
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_65005 bfd-liveness-detection multiplier 3
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_65005 neighbor 100.2.1.1 local-address 100.2.1.0
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_65005 neighbor 100.2.1.1 family inet unicast
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_65006 type external
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_65006 hold-time 12
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_65006 peer-as 65006
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_65006 neighbor 100.2.2.1 local-address 100.2.2.0
set routing-instances DC-LLC_VRF protocols bgp group DC-LLC_65006 neighbor 100.2.2.1 family inet unicast
set routing-instances DC-LLC_VRF interface ge-0/0/8.0
set routing-instances DC-LLC_VRF interface ge-0/0/9.0
set routing-instances DC-LLC_VRF vrf-import DC-LLC_IMPORT
set routing-instances DC-LLC_VRF vrf-export DC-LLC_EXPORT
set routing-instances DC-LLC_VRF vrf-target target:64512:101
set routing-options route-distinguisher-id 192.168.255.3
set routing-options router-id 192.168.255.3
set routing-options autonomous-system 64512
set protocols router-advertisement interface fxp0.0 managed-configuration
set protocols bgp group ISP-CORE type internal
set protocols bgp group ISP-CORE local-address 192.168.255.3
set protocols bgp group ISP-CORE family inet-vpn unicast
set protocols bgp group ISP-CORE neighbor 192.168.255.2
set protocols bgp group ISP-CORE neighbor 192.168.255.1
set protocols ldp interface ge-0/0/1.0
set protocols ldp interface lo0.0
set protocols mpls interface ge-0/0/1.0
set protocols ospf area 0.0.0.0 interface ge-0/0/1.0 interface-type p2p
set protocols ospf area 0.0.0.0 interface lo0.0 passive
set protocols ospf reference-bandwidth 100g
```
