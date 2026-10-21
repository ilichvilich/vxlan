### SPINE-A1
```
root@SPINE-A1> show route

inet.0: 14 destinations, 20 routes (14 active, 0 holddown, 1 hidden)
+ = Active Route, - = Last Active, * = Both

100.1.1.0/31       *[Direct/0] 3d 10:34:58
                    >  via ge-0/0/9.0
100.1.1.1/32       *[Local/0] 3d 10:34:58
                       Local via ge-0/0/9.0
172.16.11.0/31     *[Direct/0] 2d 11:06:22
                    >  via ge-0/0/1.0
172.16.11.0/32     *[Local/0] 2d 11:06:22
                       Local via ge-0/0/1.0
172.16.12.0/31     *[Direct/0] 2d 11:06:22
                    >  via ge-0/0/2.0
172.16.12.0/32     *[Local/0] 2d 11:06:22
                       Local via ge-0/0/2.0
192.168.1.1/32     *[Direct/0] 3d 09:00:11
                    >  via lo0.0
192.168.1.2/32     *[BGP/170] 06:07:37, localpref 100, from 172.16.11.1
                      AS path: 65003 65002 I, validation-state: unverified
                       to 172.16.11.1 via ge-0/0/1.0
                    >  to 172.16.12.1 via ge-0/0/2.0
                    [BGP/170] 2d 07:43:53, localpref 100
                      AS path: 65004 65002 I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
192.168.1.3/32     *[BGP/170] 2d 07:43:53, localpref 100
                      AS path: 65003 I, validation-state: unverified
                    >  to 172.16.11.1 via ge-0/0/1.0
192.168.1.4/32     *[BGP/170] 2d 07:43:53, localpref 100
                      AS path: 65004 I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
192.168.1.5/32     *[BGP/170] 00:53:31, localpref 150
                      AS path: 64512 65005 I, validation-state: unverified
                    >  to 100.1.1.0 via ge-0/0/9.0
                    [BGP/170] 00:53:30, localpref 100
                      AS path: 65003 65002 64512 65005 I, validation-state: unverified
                    >  to 172.16.11.1 via ge-0/0/1.0
                    [BGP/170] 00:53:30, localpref 100
                      AS path: 65004 65002 64512 65005 I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
192.168.1.6/32     *[BGP/170] 01:00:27, localpref 150
                      AS path: 64512 65006 I, validation-state: unverified
                    >  to 100.1.1.0 via ge-0/0/9.0
                    [BGP/170] 01:00:26, localpref 100
                      AS path: 65003 65002 64512 65006 I, validation-state: unverified
                    >  to 172.16.11.1 via ge-0/0/1.0
                    [BGP/170] 01:00:26, localpref 100
                      AS path: 65004 65002 64512 65006 I, validation-state: unverified
                    >  to 172.16.12.1 via ge-0/0/2.0
192.168.1.7/32     *[BGP/170] 00:59:48, localpref 150
                      AS path: 64512 65006 65007 I, validation-state: unverified
                    >  to 100.1.1.0 via ge-0/0/9.0
192.168.1.8/32     *[BGP/170] 00:59:48, localpref 150
                      AS path: 64512 65006 65008 I, validation-state: unverified
                    >  to 100.1.1.0 via ge-0/0/9.0

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe04:0/128
                   *[Local/0] 3d 21:03:50
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 3d 21:04:01
                       MultiRecv
```

### SPINE-A2
```
root@SPINE-A2> show route

inet.0: 14 destinations, 24 routes (14 active, 0 holddown, 3 hidden)
+ = Active Route, - = Last Active, * = Both

100.1.2.0/31       *[Direct/0] 3d 08:03:43
                    >  via ge-0/0/8.0
100.1.2.1/32       *[Local/0] 3d 08:03:43
                       Local via ge-0/0/8.0
172.16.21.0/31     *[Direct/0] 2d 11:06:18
                    >  via ge-0/0/1.0
172.16.21.0/32     *[Local/0] 2d 11:06:18
                       Local via ge-0/0/1.0
172.16.22.0/31     *[Direct/0] 2d 11:06:18
                    >  via ge-0/0/2.0
172.16.22.0/32     *[Local/0] 2d 11:06:18
                       Local via ge-0/0/2.0
192.168.1.1/32     *[BGP/170] 2d 07:44:26, localpref 100, from 172.16.21.1
                      AS path: 65003 65001 I, validation-state: unverified
                       to 172.16.21.1 via ge-0/0/1.0
                    >  to 172.16.22.1 via ge-0/0/2.0
                    [BGP/170] 2d 07:44:26, localpref 100
                      AS path: 65004 65001 I, validation-state: unverified
                    >  to 172.16.22.1 via ge-0/0/2.0
192.168.1.2/32     *[Direct/0] 2d 09:03:23
                    >  via lo0.0
192.168.1.3/32     *[BGP/170] 2d 07:44:26, localpref 100
                      AS path: 65003 I, validation-state: unverified
                    >  to 172.16.21.1 via ge-0/0/1.0
                    [BGP/170] 2d 07:44:26, localpref 100
                      AS path: 65004 65001 65003 I, validation-state: unverified
                    >  to 172.16.22.1 via ge-0/0/2.0
192.168.1.4/32     *[BGP/170] 2d 07:44:26, localpref 100
                      AS path: 65004 I, validation-state: unverified
                    >  to 172.16.22.1 via ge-0/0/2.0
                    [BGP/170] 2d 07:44:26, localpref 100
                      AS path: 65003 65001 65004 I, validation-state: unverified
                    >  to 172.16.21.1 via ge-0/0/1.0
192.168.1.5/32     *[BGP/170] 00:54:03, localpref 100
                      AS path: 64512 65005 I, validation-state: unverified
                    >  to 100.1.2.0 via ge-0/0/8.0
192.168.1.6/32     *[BGP/170] 01:00:59, localpref 100
                      AS path: 64512 65006 I, validation-state: unverified
                    >  to 100.1.2.0 via ge-0/0/8.0
192.168.1.7/32     *[BGP/170] 01:00:21, localpref 100
                      AS path: 64512 65006 65007 I, validation-state: unverified
                    >  to 100.1.2.0 via ge-0/0/8.0
                    [BGP/170] 01:00:20, localpref 100
                      AS path: 65003 65001 64512 65006 65007 I, validation-state: unverified
                    >  to 172.16.21.1 via ge-0/0/1.0
                    [BGP/170] 01:00:20, localpref 100
                      AS path: 65004 65001 64512 65006 65007 I, validation-state: unverified
                    >  to 172.16.22.1 via ge-0/0/2.0
192.168.1.8/32     *[BGP/170] 01:00:21, localpref 100
                      AS path: 64512 65006 65008 I, validation-state: unverified
                    >  to 100.1.2.0 via ge-0/0/8.0
                    [BGP/170] 01:00:20, localpref 100
                      AS path: 65003 65001 64512 65006 65008 I, validation-state: unverified
                    >  to 172.16.21.1 via ge-0/0/1.0
                    [BGP/170] 01:00:20, localpref 100
                      AS path: 65004 65001 64512 65006 65008 I, validation-state: unverified
                    >  to 172.16.22.1 via ge-0/0/2.0

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe05:0/128
                   *[Local/0] 3d 08:06:48
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 3d 08:06:59
                       MultiRecv
```
### LEAF-A1
```
root@LEAF-A1> show route

inet.0: 12 destinations, 17 routes (12 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

172.16.11.0/31     *[Direct/0] 2d 07:58:44
                    >  via ge-0/0/1.0
172.16.11.1/32     *[Local/0] 2d 07:58:44
                       Local via ge-0/0/1.0
172.16.21.0/31     *[Direct/0] 2d 07:58:44
                    >  via ge-0/0/2.0
172.16.21.1/32     *[Local/0] 2d 07:58:44
                       Local via ge-0/0/2.0
192.168.1.1/32     *[BGP/170] 2d 07:44:48, localpref 100
                      AS path: 65001 I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
192.168.1.2/32     *[BGP/170] 2d 07:44:48, localpref 100
                      AS path: 65002 I, validation-state: unverified
                    >  to 172.16.21.0 via ge-0/0/2.0
192.168.1.3/32     *[Direct/0] 2d 07:58:44
                    >  via lo0.0
192.168.1.4/32     *[BGP/170] 2d 07:44:48, localpref 100, from 172.16.11.0
                      AS path: 65001 65004 I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
                    [BGP/170] 2d 07:44:48, localpref 100
                      AS path: 65002 65004 I, validation-state: unverified
                    >  to 172.16.21.0 via ge-0/0/2.0
192.168.1.5/32     *[BGP/170] 00:54:23, localpref 100
                      AS path: 65002 64512 65005 I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
                    [BGP/170] 00:54:23, localpref 100
                      AS path: 65001 64512 65005 I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
192.168.1.6/32     *[BGP/170] 01:01:19, localpref 100
                      AS path: 65002 64512 65006 I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
                    [BGP/170] 01:01:19, localpref 100
                      AS path: 65001 64512 65006 I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
192.168.1.7/32     *[BGP/170] 01:00:41, localpref 100, from 172.16.11.0
                      AS path: 65001 64512 65006 65007 I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
                    [BGP/170] 01:00:41, localpref 100
                      AS path: 65002 64512 65006 65007 I, validation-state: unverified
                    >  to 172.16.21.0 via ge-0/0/2.0
192.168.1.8/32     *[BGP/170] 01:00:41, localpref 100
                      AS path: 65001 64512 65006 65008 I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
                    [BGP/170] 01:00:41, localpref 100
                      AS path: 65002 64512 65006 65008 I, validation-state: unverified
                    >  to 172.16.21.0 via ge-0/0/2.0

RED-L3PVN-VRF.inet.0: 4 destinations, 6 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.100.10.0/24     *[Direct/0] 09:48:46
                    >  via irb.10
                    [EVPN/170] 1d 08:45:01
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
10.100.10.1/32     *[EVPN/7] 1d 08:44:54
                    >  via irb.10
10.100.10.253/32   *[Local/0] 09:48:46
                       Local via irb.10
10.100.20.0/24     *[EVPN/170] 01:09:09
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
                    [EVPN/170] 01:09:09
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0

GREEN-L3PVN-VRF.inet.0: 4 destinations, 6 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.200.10.0/24     *[Direct/0] 10:26:04
                    >  via irb.20
                    [EVPN/170] 10:08:09
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
10.200.10.1/32     *[EVPN/7] 09:43:48
                    >  via irb.20
10.200.10.253/32   *[Local/0] 10:26:04
                       Local via irb.20
10.200.20.0/24     *[EVPN/170] 01:09:09
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
                    [EVPN/170] 01:09:09
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe08:0/128
                   *[Local/0] 2d 08:00:42
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 2d 08:00:53
                       MultiRecv

bgp.evpn.0: 96 destinations, 96 routes (96 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 2d 07:23:07
                       Indirect
1:192.168.1.3:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 09:45:13
                       Indirect
1:192.168.1.3:0::050000fdeb0000139200::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 09:48:45
                       Indirect
1:192.168.1.3:0::050000fdeb0000139c00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 10:26:04
                       Indirect
1:192.168.1.3:9::010000000000000001::0/192 AD/EVI
                   *[EVPN/170] 2d 07:23:18
                       Indirect
1:192.168.1.3:12::010000000000000002::0/192 AD/EVI
                   *[EVPN/170] 09:45:24
                       Indirect
1:192.168.1.4:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 07:23:11, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.4:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 10:04:26, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.4:0::050000fdec0000139200::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 09:48:49, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.4:0::050000fdec0000139c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 10:08:09, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.4:9::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 1d 09:26:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 5010
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 5010
1:192.168.1.4:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 10:03:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 5020
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 5020
1:192.168.1.7:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.7:0::020000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.7:0::050000fdef0000139300::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.7:0::050000fdef0000139d00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.7:11::020000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
1:192.168.1.7:12::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
1:192.168.1.8:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.8:0::020000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.8:0::050000fdf00000139300::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.8:0::050000fdf00000139d00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.8:8::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
1:192.168.1.8:11::020000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 09:48:45
                       Indirect
2:192.168.1.3:9::0::2c:6b:f5:d2:9c:f0/304 MAC/IP
                   *[EVPN/170] 1d 08:45:01
                       Indirect
2:192.168.1.3:9::0::aa:bb:cc:00:c0:10/304 MAC/IP
                   *[EVPN/170] 2d 07:23:22
                       Indirect
2:192.168.1.3:9::0::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[EVPN/170] 2d 02:55:04
                       Indirect
2:192.168.1.3:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 10:26:04
                       Indirect
2:192.168.1.3:12::0::2c:6b:f5:d2:9c:f0/304 MAC/IP
                   *[EVPN/170] 12:06:42
                       Indirect
2:192.168.1.3:12::0::aa:bb:cc:00:d0:10/304 MAC/IP
                   *[EVPN/170] 09:45:27
                       Indirect
2:192.168.1.3:12::0::aa:bb:cc:80:d0:00/304 MAC/IP
                   *[EVPN/170] 09:43:49
                       Indirect
2:192.168.1.4:9::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 09:48:49, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::2c:6b:f5:fc:c8:f0/304 MAC/IP
                   *[BGP/170] 2d 07:23:23, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 5010
                       to 172.16.21.0 via ge-0/0/2.0, Push 5010
2:192.168.1.4:9::0::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 12:06:46, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 5010
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 5010
2:192.168.1.4:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 10:03:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 5020
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 5020
2:192.168.1.4:12::0::2c:6b:f5:fc:c8:f0/304 MAC/IP
                   *[BGP/170] 10:03:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 5020
                       to 172.16.21.0 via ge-0/0/2.0, Push 5020
2:192.168.1.4:12::0::aa:bb:cc:80:d0:00/304 MAC/IP
                   *[BGP/170] 09:43:49, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::2c:6b:f5:fb:e9:f0/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::aa:bb:cc:00:f0:10/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::aa:bb:cc:80:f0:00/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::2c:6b:f5:fb:e9:f0/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::aa:bb:cc:00:e0:10/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::aa:bb:cc:80:e0:00/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::2c:6b:f5:cd:68:f0/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::aa:bb:cc:80:e0:00/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::2c:6b:f5:cd:68:f0/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::aa:bb:cc:80:f0:00/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::00:00:5e:00:01:01::10.100.10.254/304 MAC/IP
                   *[EVPN/170] 09:48:45
                       Indirect
2:192.168.1.3:9::0::2c:6b:f5:d2:9c:f0::10.100.10.253/304 MAC/IP
                   *[EVPN/170] 09:48:46
                       Indirect
2:192.168.1.3:9::0::aa:bb:cc:80:c0:00::10.100.10.1/304 MAC/IP
                   *[EVPN/170] 1d 08:44:55
                       Indirect
2:192.168.1.3:12::0::00:00:5e:00:01:01::10.200.10.254/304 MAC/IP
                   *[EVPN/170] 10:26:04
                       Indirect
2:192.168.1.3:12::0::2c:6b:f5:d2:9c:f0::10.200.10.253/304 MAC/IP
                   *[EVPN/170] 10:26:04
                       Indirect
2:192.168.1.3:12::0::aa:bb:cc:80:d0:00::10.200.10.1/304 MAC/IP
                   *[EVPN/170] 09:43:49
                       Indirect
2:192.168.1.4:9::0::00:00:5e:00:01:01::10.100.10.254/304 MAC/IP
                   *[BGP/170] 09:48:49, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::2c:6b:f5:fc:c8:f0::10.100.10.252/304 MAC/IP
                   *[BGP/170] 09:48:49, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::aa:bb:cc:80:c0:00::10.100.10.1/304 MAC/IP
                   *[BGP/170] 12:06:46, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 5010
                       to 172.16.21.0 via ge-0/0/2.0, Push 5010
2:192.168.1.4:12::0::00:00:5e:00:01:01::10.200.10.254/304 MAC/IP
                   *[BGP/170] 10:03:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 5020
                       to 172.16.21.0 via ge-0/0/2.0, Push 5020
2:192.168.1.4:12::0::2c:6b:f5:fc:c8:f0::10.200.10.252/304 MAC/IP
                   *[BGP/170] 10:03:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 5020
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 5020
2:192.168.1.4:12::0::aa:bb:cc:80:d0:00::10.200.10.1/304 MAC/IP
                   *[BGP/170] 09:43:48, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::00:00:5e:00:01:01::10.200.20.254/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::2c:6b:f5:fb:e9:f0::10.200.20.253/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::aa:bb:cc:80:f0:00::10.200.20.1/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::00:00:5e:00:01:01::10.100.20.254/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::2c:6b:f5:fb:e9:f0::10.100.20.253/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::aa:bb:cc:80:e0:00::10.100.20.1/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::00:00:5e:00:01:01::10.100.20.254/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::2c:6b:f5:cd:68:f0::10.100.20.252/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::aa:bb:cc:80:e0:00::10.100.20.1/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::00:00:5e:00:01:01::10.200.20.254/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::2c:6b:f5:cd:68:f0::10.200.20.252/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::aa:bb:cc:80:f0:00::10.200.20.1/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
3:192.168.1.3:9::0::192.168.1.3/248 IM
                   *[EVPN/170] 2d 07:23:21
                       Indirect
3:192.168.1.3:12::0::192.168.1.3/248 IM
                   *[EVPN/170] 12:06:45
                       Indirect
3:192.168.1.4:9::0::192.168.1.4/248 IM
                   *[BGP/170] 10:03:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
3:192.168.1.4:12::0::192.168.1.4/248 IM
                   *[BGP/170] 10:03:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
3:192.168.1.7:11::0::192.168.1.7/248 IM
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
3:192.168.1.7:12::0::192.168.1.7/248 IM
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
3:192.168.1.8:8::0::192.168.1.8/248 IM
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
3:192.168.1.8:11::0::192.168.1.8/248 IM
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
4:192.168.1.3:0::010000000000000001:192.168.1.3/296 ES
                   *[EVPN/170] 2d 07:23:08
                       Indirect
4:192.168.1.3:0::010000000000000002:192.168.1.3/296 ES
                   *[EVPN/170] 09:45:14
                       Indirect
4:192.168.1.4:0::010000000000000001:192.168.1.4/296 ES
                   *[BGP/170] 2d 07:23:12, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
4:192.168.1.4:0::010000000000000002:192.168.1.4/296 ES
                   *[BGP/170] 10:04:27, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
5:192.168.1.3:10::0::10.100.10.0::24/248
                   *[EVPN/170] 1d 08:45:01
                       Fictitious
5:192.168.1.3:11::0::10.200.10.0::24/248
                   *[EVPN/170] 12:00:15
                       Fictitious
5:192.168.1.4:10::0::10.100.10.0::24/248
                   *[BGP/170] 12:06:46, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 5100
5:192.168.1.4:11::0::10.200.10.0::24/248
                   *[BGP/170] 10:08:09, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 325
                       to 172.16.21.0 via ge-0/0/2.0, Push 325
5:192.168.1.7:9::0::10.100.20.0::24/248
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 318
                       to 172.16.21.0 via ge-0/0/2.0, Push 318
5:192.168.1.7:10::0::10.200.20.0::24/248
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 325
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 325
5:192.168.1.8:9::0::10.100.20.0::24/248
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 318
5:192.168.1.8:10::0::10.200.20.0::24/248
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 325
                       to 172.16.21.0 via ge-0/0/2.0, Push 325

RED-L3PVN-VRF.evpn.0: 4 destinations, 4 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

5:192.168.1.3:10::0::10.100.10.0::24/248
                   *[EVPN/170] 1d 08:45:01
                       Fictitious
5:192.168.1.4:10::0::10.100.10.0::24/248
                   *[BGP/170] 12:06:46, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 5100
5:192.168.1.7:9::0::10.100.20.0::24/248
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 318
                       to 172.16.21.0 via ge-0/0/2.0, Push 318
5:192.168.1.8:9::0::10.100.20.0::24/248
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 318

__default_evpn__.evpn.0: 8 destinations, 8 routes (8 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 2d 07:23:07
                       Indirect
1:192.168.1.3:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 09:45:13
                       Indirect
1:192.168.1.3:0::050000fdeb0000139200::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 09:48:45
                       Indirect
1:192.168.1.3:0::050000fdeb0000139c00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 10:26:04
                       Indirect
4:192.168.1.3:0::010000000000000001:192.168.1.3/296 ES
                   *[EVPN/170] 2d 07:23:08
                       Indirect
4:192.168.1.3:0::010000000000000002:192.168.1.3/296 ES
                   *[EVPN/170] 09:45:14
                       Indirect
4:192.168.1.4:0::010000000000000001:192.168.1.4/296 ES
                   *[BGP/170] 2d 07:23:12, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
4:192.168.1.4:0::010000000000000002:192.168.1.4/296 ES
                   *[BGP/170] 10:04:27, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0

RED-VLAN-BASED-EVI.evpn.0: 40 destinations, 40 routes (40 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:9::010000000000000001::0/192 AD/EVI
                   *[EVPN/170] 2d 07:23:18
                       Indirect
1:192.168.1.4:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 07:23:11, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.4:0::050000fdec0000139200::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 09:48:49, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.4:9::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 1d 09:26:59, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 5010
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 5010
1:192.168.1.7:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.7:0::050000fdef0000139300::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.7:12::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
1:192.168.1.8:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.8:0::050000fdf00000139300::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.8:8::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 09:48:45
                       Indirect
2:192.168.1.3:9::0::2c:6b:f5:d2:9c:f0/304 MAC/IP
                   *[EVPN/170] 1d 08:45:01
                       Indirect
2:192.168.1.3:9::0::aa:bb:cc:00:c0:10/304 MAC/IP
                   *[EVPN/170] 2d 07:23:22
                       Indirect
2:192.168.1.3:9::0::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[EVPN/170] 2d 02:55:04
                       Indirect
2:192.168.1.4:9::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 09:48:49, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::2c:6b:f5:fc:c8:f0/304 MAC/IP
                   *[BGP/170] 2d 07:23:23, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 5010
                       to 172.16.21.0 via ge-0/0/2.0, Push 5010
2:192.168.1.4:9::0::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 12:06:46, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 5010
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 5010
2:192.168.1.7:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::2c:6b:f5:fb:e9:f0/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::aa:bb:cc:00:e0:10/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::aa:bb:cc:80:e0:00/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::2c:6b:f5:cd:68:f0/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::aa:bb:cc:80:e0:00/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::00:00:5e:00:01:01::10.100.10.254/304 MAC/IP
                   *[EVPN/170] 09:48:45
                       Indirect
2:192.168.1.3:9::0::2c:6b:f5:d2:9c:f0::10.100.10.253/304 MAC/IP
                   *[EVPN/170] 09:48:46
                       Indirect
2:192.168.1.3:9::0::aa:bb:cc:80:c0:00::10.100.10.1/304 MAC/IP
                   *[EVPN/170] 1d 08:44:55
                       Indirect
2:192.168.1.4:9::0::00:00:5e:00:01:01::10.100.10.254/304 MAC/IP
                   *[BGP/170] 09:48:49, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::2c:6b:f5:fc:c8:f0::10.100.10.252/304 MAC/IP
                   *[BGP/170] 09:48:49, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::aa:bb:cc:80:c0:00::10.100.10.1/304 MAC/IP
                   *[BGP/170] 12:06:46, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 5010
                       to 172.16.21.0 via ge-0/0/2.0, Push 5010
2:192.168.1.7:12::0::00:00:5e:00:01:01::10.100.20.254/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::2c:6b:f5:fb:e9:f0::10.100.20.253/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::aa:bb:cc:80:e0:00::10.100.20.1/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::00:00:5e:00:01:01::10.100.20.254/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::2c:6b:f5:cd:68:f0::10.100.20.252/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::aa:bb:cc:80:e0:00::10.100.20.1/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
3:192.168.1.3:9::0::192.168.1.3/248 IM
                   *[EVPN/170] 2d 07:23:21
                       Indirect
3:192.168.1.4:9::0::192.168.1.4/248 IM
                   *[BGP/170] 10:03:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
3:192.168.1.7:12::0::192.168.1.7/248 IM
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
3:192.168.1.8:8::0::192.168.1.8/248 IM
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0

GREEN-L3PVN-VRF.evpn.0: 4 destinations, 4 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

5:192.168.1.3:11::0::10.200.10.0::24/248
                   *[EVPN/170] 12:00:15
                       Fictitious
5:192.168.1.4:11::0::10.200.10.0::24/248
                   *[BGP/170] 10:08:09, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 325
                       to 172.16.21.0 via ge-0/0/2.0, Push 325
5:192.168.1.7:10::0::10.200.20.0::24/248
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 325
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 325
5:192.168.1.8:10::0::10.200.20.0::24/248
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 325
                       to 172.16.21.0 via ge-0/0/2.0, Push 325

GREEN-VLAN-BASED-EVI.evpn.0: 40 destinations, 40 routes (40 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:12::010000000000000002::0/192 AD/EVI
                   *[EVPN/170] 09:45:24
                       Indirect
1:192.168.1.4:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 10:04:26, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.4:0::050000fdec0000139c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 10:08:09, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.4:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 10:03:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 5020
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 5020
1:192.168.1.7:0::020000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0
                       to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.7:0::050000fdef0000139d00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.7:11::020000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
1:192.168.1.8:0::020000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.8:0::050000fdf00000139d00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
1:192.168.1.8:11::020000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 10:26:04
                       Indirect
2:192.168.1.3:12::0::2c:6b:f5:d2:9c:f0/304 MAC/IP
                   *[EVPN/170] 12:06:42
                       Indirect
2:192.168.1.3:12::0::aa:bb:cc:00:d0:10/304 MAC/IP
                   *[EVPN/170] 09:45:27
                       Indirect
2:192.168.1.3:12::0::aa:bb:cc:80:d0:00/304 MAC/IP
                   *[EVPN/170] 09:43:49
                       Indirect
2:192.168.1.4:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 10:03:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 5020
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 5020
2:192.168.1.4:12::0::2c:6b:f5:fc:c8:f0/304 MAC/IP
                   *[BGP/170] 10:03:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 5020
                       to 172.16.21.0 via ge-0/0/2.0, Push 5020
2:192.168.1.4:12::0::aa:bb:cc:80:d0:00/304 MAC/IP
                   *[BGP/170] 09:43:49, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::2c:6b:f5:fb:e9:f0/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::aa:bb:cc:00:f0:10/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::aa:bb:cc:80:f0:00/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::2c:6b:f5:cd:68:f0/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::aa:bb:cc:80:f0:00/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::00:00:5e:00:01:01::10.200.10.254/304 MAC/IP
                   *[EVPN/170] 10:26:04
                       Indirect
2:192.168.1.3:12::0::2c:6b:f5:d2:9c:f0::10.200.10.253/304 MAC/IP
                   *[EVPN/170] 10:26:04
                       Indirect
2:192.168.1.3:12::0::aa:bb:cc:80:d0:00::10.200.10.1/304 MAC/IP
                   *[EVPN/170] 09:43:49
                       Indirect
2:192.168.1.4:12::0::00:00:5e:00:01:01::10.200.10.254/304 MAC/IP
                   *[BGP/170] 10:03:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 5020
                       to 172.16.21.0 via ge-0/0/2.0, Push 5020
2:192.168.1.4:12::0::2c:6b:f5:fc:c8:f0::10.200.10.252/304 MAC/IP
                   *[BGP/170] 10:03:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 5020
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 5020
2:192.168.1.4:12::0::aa:bb:cc:80:d0:00::10.200.10.1/304 MAC/IP
                   *[BGP/170] 09:43:48, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::00:00:5e:00:01:01::10.200.20.254/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::2c:6b:f5:fb:e9:f0::10.200.20.253/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::aa:bb:cc:80:f0:00::10.200.20.1/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::00:00:5e:00:01:01::10.200.20.254/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.11.0 via ge-0/0/1.0, Push 313
                       to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::2c:6b:f5:cd:68:f0::10.200.20.252/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::aa:bb:cc:80:f0:00::10.200.20.1/304 MAC/IP
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.21.0 via ge-0/0/2.0, Push 313
3:192.168.1.3:12::0::192.168.1.3/248 IM
                   *[EVPN/170] 12:06:45
                       Indirect
3:192.168.1.4:12::0::192.168.1.4/248 IM
                   *[BGP/170] 10:03:07, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
3:192.168.1.7:11::0::192.168.1.7/248 IM
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
3:192.168.1.8:11::0::192.168.1.8/248 IM
                   *[BGP/170] 01:09:09, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.11.0 via ge-0/0/1.0
                    >  to 172.16.21.0 via ge-0/0/2.0
```
### LEAF-A2
```
root@LEAF-A2> show route | no-more

inet.0: 12 destinations, 19 routes (12 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

172.16.12.0/31     *[Direct/0] 2d 07:58:42
                    >  via ge-0/0/1.0
172.16.12.1/32     *[Local/0] 2d 07:58:42
                       Local via ge-0/0/1.0
172.16.22.0/31     *[Direct/0] 2d 07:58:42
                    >  via ge-0/0/2.0
172.16.22.1/32     *[Local/0] 2d 07:58:42
                       Local via ge-0/0/2.0
192.168.1.1/32     *[BGP/170] 2d 07:45:45, localpref 100
                      AS path: 65001 I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                    [BGP/170] 2d 07:45:45, localpref 100
                      AS path: 65002 65003 65001 I, validation-state: unverified
                    >  to 172.16.22.0 via ge-0/0/2.0
192.168.1.2/32     *[BGP/170] 2d 07:45:45, localpref 100
                      AS path: 65002 I, validation-state: unverified
                    >  to 172.16.22.0 via ge-0/0/2.0
                    [BGP/170] 06:09:25, localpref 100
                      AS path: 65001 65003 65002 I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
192.168.1.3/32     *[BGP/170] 2d 07:45:45, localpref 100, from 172.16.12.0
                      AS path: 65001 65003 I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
                    [BGP/170] 2d 07:45:45, localpref 100
                      AS path: 65002 65003 I, validation-state: unverified
                    >  to 172.16.22.0 via ge-0/0/2.0
192.168.1.4/32     *[Direct/0] 2d 07:58:42
                    >  via lo0.0
192.168.1.5/32     *[BGP/170] 00:55:18, localpref 100
                      AS path: 65002 64512 65005 I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
                    [BGP/170] 00:55:18, localpref 100
                      AS path: 65001 64512 65005 I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
192.168.1.6/32     *[BGP/170] 01:02:14, localpref 100
                      AS path: 65002 64512 65006 I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
                    [BGP/170] 01:02:14, localpref 100
                      AS path: 65001 64512 65006 I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
192.168.1.7/32     *[BGP/170] 01:01:36, localpref 100, from 172.16.12.0
                      AS path: 65001 64512 65006 65007 I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
                    [BGP/170] 01:01:36, localpref 100
                      AS path: 65002 64512 65006 65007 I, validation-state: unverified
                    >  to 172.16.22.0 via ge-0/0/2.0
192.168.1.8/32     *[BGP/170] 01:01:36, localpref 100
                      AS path: 65001 64512 65006 65008 I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
                    [BGP/170] 01:01:36, localpref 100
                      AS path: 65002 64512 65006 65008 I, validation-state: unverified
                    >  to 172.16.22.0 via ge-0/0/2.0

RED-L3PVN-VRF.inet.0: 4 destinations, 6 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.100.10.0/24     *[Direct/0] 09:49:44
                    >  via irb.10
                    [EVPN/170] 1d 08:45:56
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
10.100.10.1/32     *[EVPN/7] 1d 08:45:49
                    >  via irb.10
10.100.10.252/32   *[Local/0] 09:49:44
                       Local via irb.10
10.100.20.0/24     *[EVPN/170] 01:10:04
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
                    [EVPN/170] 01:10:04
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0

GREEN-L3PVN-VRF.inet.0: 4 destinations, 6 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.200.10.0/24     *[Direct/0] 10:09:04
                    >  via irb.20
                    [EVPN/170] 12:00:57
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
10.200.10.1/32     *[EVPN/7] 09:44:43
                    >  via irb.20
10.200.10.252/32   *[Local/0] 10:09:04
                       Local via irb.20
10.200.20.0/24     *[EVPN/170] 01:10:04
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
                    [EVPN/170] 01:10:04
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe09:0/128
                   *[Local/0] 2d 08:02:48
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 2d 08:02:59
                       MultiRecv

bgp.evpn.0: 96 destinations, 96 routes (96 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 07:24:02, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.3:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 09:46:07, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.3:0::050000fdeb0000139200::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 09:49:40, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.3:0::050000fdeb0000139c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 10:26:59, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.3:9::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 1d 09:27:45, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5010
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5010
1:192.168.1.3:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 09:46:18, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
1:192.168.1.4:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 2d 07:24:06
                       Indirect
1:192.168.1.4:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 10:05:21
                       Indirect
1:192.168.1.4:0::050000fdec0000139200::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 09:49:44
                       Indirect
1:192.168.1.4:0::050000fdec0000139c00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 10:09:04
                       Indirect
1:192.168.1.4:9::010000000000000001::0/192 AD/EVI
                   *[EVPN/170] 2d 07:24:17
                       Indirect
1:192.168.1.4:12::010000000000000002::0/192 AD/EVI
                   *[EVPN/170] 10:05:32
                       Indirect
1:192.168.1.7:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.7:0::020000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.7:0::050000fdef0000139300::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.7:0::050000fdef0000139d00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.7:11::020000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
1:192.168.1.7:12::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
1:192.168.1.8:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.8:0::020000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.8:0::050000fdf00000139300::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.8:0::050000fdf00000139d00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.8:8::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
1:192.168.1.8:11::020000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 09:49:40, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::2c:6b:f5:d2:9c:f0/304 MAC/IP
                   *[BGP/170] 1d 09:27:45, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5010
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5010
2:192.168.1.3:9::0::aa:bb:cc:00:c0:10/304 MAC/IP
                   *[BGP/170] 1d 09:27:45, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5010
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5010
2:192.168.1.3:9::0::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 1d 09:27:45, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5010
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5010
2:192.168.1.3:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 10:09:46, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5020
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5020
2:192.168.1.3:12::0::2c:6b:f5:d2:9c:f0/304 MAC/IP
                   *[BGP/170] 10:09:46, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5020
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5020
2:192.168.1.3:12::0::aa:bb:cc:00:d0:10/304 MAC/IP
                   *[BGP/170] 09:46:21, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::aa:bb:cc:80:d0:00/304 MAC/IP
                   *[BGP/170] 09:44:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 09:49:44
                       Indirect
2:192.168.1.4:9::0::2c:6b:f5:fc:c8:f0/304 MAC/IP
                   *[EVPN/170] 1d 08:45:56
                       Indirect
2:192.168.1.4:9::0::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[EVPN/170] 1d 08:45:49
                       Indirect
2:192.168.1.4:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 10:09:04
                       Indirect
2:192.168.1.4:12::0::2c:6b:f5:fc:c8:f0/304 MAC/IP
                   *[EVPN/170] 10:09:04
                       Indirect
2:192.168.1.4:12::0::aa:bb:cc:80:d0:00/304 MAC/IP
                   *[EVPN/170] 09:44:44
                       Indirect
2:192.168.1.7:11::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5021
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5021
2:192.168.1.7:11::0::2c:6b:f5:fb:e9:f0/304 MAC/IP
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 5021
                       to 172.16.22.0 via ge-0/0/2.0, Push 5021
2:192.168.1.7:11::0::aa:bb:cc:00:f0:10/304 MAC/IP
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::aa:bb:cc:80:f0:00/304 MAC/IP
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::2c:6b:f5:fb:e9:f0/304 MAC/IP
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::aa:bb:cc:00:e0:10/304 MAC/IP
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::aa:bb:cc:80:e0:00/304 MAC/IP
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::2c:6b:f5:cd:68:f0/304 MAC/IP
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::aa:bb:cc:80:e0:00/304 MAC/IP
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:10:04, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::2c:6b:f5:cd:68:f0/304 MAC/IP
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::aa:bb:cc:80:f0:00/304 MAC/IP
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::00:00:5e:00:01:01::10.100.10.254/304 MAC/IP
                   *[BGP/170] 09:49:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::2c:6b:f5:d2:9c:f0::10.100.10.253/304 MAC/IP
                   *[BGP/170] 09:49:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::aa:bb:cc:80:c0:00::10.100.10.1/304 MAC/IP
                   *[BGP/170] 12:07:39, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 5010
                       to 172.16.22.0 via ge-0/0/2.0, Push 5010
2:192.168.1.3:12::0::00:00:5e:00:01:01::10.200.10.254/304 MAC/IP
                   *[BGP/170] 10:09:47, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 5020
                       to 172.16.22.0 via ge-0/0/2.0, Push 5020
2:192.168.1.3:12::0::2c:6b:f5:d2:9c:f0::10.200.10.253/304 MAC/IP
                   *[BGP/170] 10:09:47, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 5020
                       to 172.16.22.0 via ge-0/0/2.0, Push 5020
2:192.168.1.3:12::0::aa:bb:cc:80:d0:00::10.200.10.1/304 MAC/IP
                   *[BGP/170] 09:44:45, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::00:00:5e:00:01:01::10.100.10.254/304 MAC/IP
                   *[EVPN/170] 09:49:45
                       Indirect
2:192.168.1.4:9::0::2c:6b:f5:fc:c8:f0::10.100.10.252/304 MAC/IP
                   *[EVPN/170] 09:49:45
                       Indirect
2:192.168.1.4:9::0::aa:bb:cc:80:c0:00::10.100.10.1/304 MAC/IP
                   *[EVPN/170] 1d 08:45:50
                       Indirect
2:192.168.1.4:12::0::00:00:5e:00:01:01::10.200.10.254/304 MAC/IP
                   *[EVPN/170] 10:09:05
                       Indirect
2:192.168.1.4:12::0::2c:6b:f5:fc:c8:f0::10.200.10.252/304 MAC/IP
                   *[EVPN/170] 10:09:05
                       Indirect
2:192.168.1.4:12::0::aa:bb:cc:80:d0:00::10.200.10.1/304 MAC/IP
                   *[EVPN/170] 09:44:44
                       Indirect
2:192.168.1.7:11::0::00:00:5e:00:01:01::10.200.20.254/304 MAC/IP
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5021
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5021
2:192.168.1.7:11::0::2c:6b:f5:fb:e9:f0::10.200.20.253/304 MAC/IP
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 5021
                       to 172.16.22.0 via ge-0/0/2.0, Push 5021
2:192.168.1.7:11::0::aa:bb:cc:80:f0:00::10.200.20.1/304 MAC/IP
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::00:00:5e:00:01:01::10.100.20.254/304 MAC/IP
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::2c:6b:f5:fb:e9:f0::10.100.20.253/304 MAC/IP
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::aa:bb:cc:80:e0:00::10.100.20.1/304 MAC/IP
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::00:00:5e:00:01:01::10.100.20.254/304 MAC/IP
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::2c:6b:f5:cd:68:f0::10.100.20.252/304 MAC/IP
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::aa:bb:cc:80:e0:00::10.100.20.1/304 MAC/IP
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::00:00:5e:00:01:01::10.200.20.254/304 MAC/IP
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::2c:6b:f5:cd:68:f0::10.200.20.252/304 MAC/IP
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::aa:bb:cc:80:f0:00::10.200.20.1/304 MAC/IP
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
3:192.168.1.3:9::0::192.168.1.3/248 IM
                   *[BGP/170] 10:05:37, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
3:192.168.1.3:12::0::192.168.1.3/248 IM
                   *[BGP/170] 10:05:37, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
3:192.168.1.4:9::0::192.168.1.4/248 IM
                   *[EVPN/170] 2d 07:24:21
                       Indirect
3:192.168.1.4:12::0::192.168.1.4/248 IM
                   *[EVPN/170] 10:09:04
                       Indirect
3:192.168.1.7:11::0::192.168.1.7/248 IM
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
3:192.168.1.7:12::0::192.168.1.7/248 IM
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
3:192.168.1.8:8::0::192.168.1.8/248 IM
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
3:192.168.1.8:11::0::192.168.1.8/248 IM
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
4:192.168.1.3:0::010000000000000001:192.168.1.3/296 ES
                   *[BGP/170] 2d 07:24:04, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
4:192.168.1.3:0::010000000000000002:192.168.1.3/296 ES
                   *[BGP/170] 09:46:09, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
4:192.168.1.4:0::010000000000000001:192.168.1.4/296 ES
                   *[EVPN/170] 2d 07:24:08
                       Indirect
4:192.168.1.4:0::010000000000000002:192.168.1.4/296 ES
                   *[EVPN/170] 10:05:23
                       Indirect
5:192.168.1.3:10::0::10.100.10.0::24/248
                   *[BGP/170] 12:07:39, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5100
5:192.168.1.3:11::0::10.200.10.0::24/248
                   *[BGP/170] 12:01:11, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 5200
                       to 172.16.22.0 via ge-0/0/2.0, Push 5200
5:192.168.1.4:10::0::10.100.10.0::24/248
                   *[EVPN/170] 1d 08:45:57
                       Fictitious
5:192.168.1.4:11::0::10.200.10.0::24/248
                   *[EVPN/170] 10:09:05
                       Fictitious
5:192.168.1.7:9::0::10.100.20.0::24/248
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 5100
                       to 172.16.22.0 via ge-0/0/2.0, Push 5100
5:192.168.1.7:10::0::10.200.20.0::24/248
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5200
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5200
5:192.168.1.8:9::0::10.100.20.0::24/248
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 318
5:192.168.1.8:10::0::10.200.20.0::24/248
                   *[BGP/170] 01:10:05, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 325
                       to 172.16.22.0 via ge-0/0/2.0, Push 325

RED-L3PVN-VRF.evpn.0: 4 destinations, 4 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

5:192.168.1.3:10::0::10.100.10.0::24/248
                   *[BGP/170] 12:07:40, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5100
5:192.168.1.4:10::0::10.100.10.0::24/248
                   *[EVPN/170] 1d 08:45:58
                       Fictitious
5:192.168.1.7:9::0::10.100.20.0::24/248
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 5100
                       to 172.16.22.0 via ge-0/0/2.0, Push 5100
5:192.168.1.8:9::0::10.100.20.0::24/248
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 318

__default_evpn__.evpn.0: 8 destinations, 8 routes (8 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.4:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 2d 07:24:08
                       Indirect
1:192.168.1.4:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 10:05:23
                       Indirect
1:192.168.1.4:0::050000fdec0000139200::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 09:49:46
                       Indirect
1:192.168.1.4:0::050000fdec0000139c00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 10:09:06
                       Indirect
4:192.168.1.3:0::010000000000000001:192.168.1.3/296 ES
                   *[BGP/170] 2d 07:24:05, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
4:192.168.1.3:0::010000000000000002:192.168.1.3/296 ES
                   *[BGP/170] 09:46:10, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
4:192.168.1.4:0::010000000000000001:192.168.1.4/296 ES
                   *[EVPN/170] 2d 07:24:09
                       Indirect
4:192.168.1.4:0::010000000000000002:192.168.1.4/296 ES
                   *[EVPN/170] 10:05:24
                       Indirect

RED-VLAN-BASED-EVI.evpn.0: 40 destinations, 40 routes (40 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 2d 07:24:04, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.3:0::050000fdeb0000139200::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 09:49:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.3:9::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 1d 09:27:47, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5010
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5010
1:192.168.1.4:9::010000000000000001::0/192 AD/EVI
                   *[EVPN/170] 2d 07:24:19
                       Indirect
1:192.168.1.7:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.7:0::050000fdef0000139300::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.7:12::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
1:192.168.1.8:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.8:0::050000fdf00000139300::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.8:8::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 09:49:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::2c:6b:f5:d2:9c:f0/304 MAC/IP
                   *[BGP/170] 1d 09:27:47, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5010
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5010
2:192.168.1.3:9::0::aa:bb:cc:00:c0:10/304 MAC/IP
                   *[BGP/170] 1d 09:27:47, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5010
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5010
2:192.168.1.3:9::0::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 1d 09:27:47, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5010
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5010
2:192.168.1.4:9::0::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 09:49:46
                       Indirect
2:192.168.1.4:9::0::2c:6b:f5:fc:c8:f0/304 MAC/IP
                   *[EVPN/170] 1d 08:45:58
                       Indirect
2:192.168.1.4:9::0::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[EVPN/170] 1d 08:45:51
                       Indirect
2:192.168.1.7:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::2c:6b:f5:fb:e9:f0/304 MAC/IP
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::aa:bb:cc:00:e0:10/304 MAC/IP
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::aa:bb:cc:80:e0:00/304 MAC/IP
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::2c:6b:f5:cd:68:f0/304 MAC/IP
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::aa:bb:cc:80:e0:00/304 MAC/IP
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::00:00:5e:00:01:01::10.100.10.254/304 MAC/IP
                   *[BGP/170] 09:49:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::2c:6b:f5:d2:9c:f0::10.100.10.253/304 MAC/IP
                   *[BGP/170] 09:49:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::aa:bb:cc:80:c0:00::10.100.10.1/304 MAC/IP
                   *[BGP/170] 12:07:40, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 5010
                       to 172.16.22.0 via ge-0/0/2.0, Push 5010
2:192.168.1.4:9::0::00:00:5e:00:01:01::10.100.10.254/304 MAC/IP
                   *[EVPN/170] 09:49:46
                       Indirect
2:192.168.1.4:9::0::2c:6b:f5:fc:c8:f0::10.100.10.252/304 MAC/IP
                   *[EVPN/170] 09:49:46
                       Indirect
2:192.168.1.4:9::0::aa:bb:cc:80:c0:00::10.100.10.1/304 MAC/IP
                   *[EVPN/170] 1d 08:45:51
                       Indirect
2:192.168.1.7:12::0::00:00:5e:00:01:01::10.100.20.254/304 MAC/IP
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::2c:6b:f5:fb:e9:f0::10.100.20.253/304 MAC/IP
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::aa:bb:cc:80:e0:00::10.100.20.1/304 MAC/IP
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::00:00:5e:00:01:01::10.100.20.254/304 MAC/IP
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::2c:6b:f5:cd:68:f0::10.100.20.252/304 MAC/IP
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::aa:bb:cc:80:e0:00::10.100.20.1/304 MAC/IP
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
3:192.168.1.3:9::0::192.168.1.3/248 IM
                   *[BGP/170] 10:05:38, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
3:192.168.1.4:9::0::192.168.1.4/248 IM
                   *[EVPN/170] 2d 07:24:22
                       Indirect
3:192.168.1.7:12::0::192.168.1.7/248 IM
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
3:192.168.1.8:8::0::192.168.1.8/248 IM
                   *[BGP/170] 01:10:06, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0

GREEN-L3PVN-VRF.evpn.0: 4 destinations, 4 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

5:192.168.1.3:11::0::10.200.10.0::24/248
                   *[BGP/170] 12:01:13, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 5200
                       to 172.16.22.0 via ge-0/0/2.0, Push 5200
5:192.168.1.4:11::0::10.200.10.0::24/248
                   *[EVPN/170] 10:09:07
                       Fictitious
5:192.168.1.7:10::0::10.200.20.0::24/248
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5200
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5200
5:192.168.1.8:10::0::10.200.20.0::24/248
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 325
                       to 172.16.22.0 via ge-0/0/2.0, Push 325

GREEN-VLAN-BASED-EVI.evpn.0: 40 destinations, 40 routes (40 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 09:46:10, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.3:0::050000fdeb0000139c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 10:27:02, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.3:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 09:46:21, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
1:192.168.1.4:12::010000000000000002::0/192 AD/EVI
                   *[EVPN/170] 10:05:35
                       Indirect
1:192.168.1.7:0::020000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0
                       to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.7:0::050000fdef0000139d00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.7:11::020000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
1:192.168.1.8:0::020000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.8:0::050000fdf00000139d00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
1:192.168.1.8:11::020000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 10:09:49, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5020
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5020
2:192.168.1.3:12::0::2c:6b:f5:d2:9c:f0/304 MAC/IP
                   *[BGP/170] 10:09:49, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5020
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5020
2:192.168.1.3:12::0::aa:bb:cc:00:d0:10/304 MAC/IP
                   *[BGP/170] 09:46:24, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::aa:bb:cc:80:d0:00/304 MAC/IP
                   *[BGP/170] 09:44:47, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 10:09:07
                       Indirect
2:192.168.1.4:12::0::2c:6b:f5:fc:c8:f0/304 MAC/IP
                   *[EVPN/170] 10:09:07
                       Indirect
2:192.168.1.4:12::0::aa:bb:cc:80:d0:00/304 MAC/IP
                   *[EVPN/170] 09:44:47
                       Indirect
2:192.168.1.7:11::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5021
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5021
2:192.168.1.7:11::0::2c:6b:f5:fb:e9:f0/304 MAC/IP
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 5021
                       to 172.16.22.0 via ge-0/0/2.0, Push 5021
2:192.168.1.7:11::0::aa:bb:cc:00:f0:10/304 MAC/IP
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::aa:bb:cc:80:f0:00/304 MAC/IP
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::2c:6b:f5:cd:68:f0/304 MAC/IP
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::aa:bb:cc:80:f0:00/304 MAC/IP
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::00:00:5e:00:01:01::10.200.10.254/304 MAC/IP
                   *[BGP/170] 10:09:49, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 5020
                       to 172.16.22.0 via ge-0/0/2.0, Push 5020
2:192.168.1.3:12::0::2c:6b:f5:d2:9c:f0::10.200.10.253/304 MAC/IP
                   *[BGP/170] 10:09:49, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 5020
                       to 172.16.22.0 via ge-0/0/2.0, Push 5020
2:192.168.1.3:12::0::aa:bb:cc:80:d0:00::10.200.10.1/304 MAC/IP
                   *[BGP/170] 09:44:47, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:12::0::00:00:5e:00:01:01::10.200.10.254/304 MAC/IP
                   *[EVPN/170] 10:09:07
                       Indirect
2:192.168.1.4:12::0::2c:6b:f5:fc:c8:f0::10.200.10.252/304 MAC/IP
                   *[EVPN/170] 10:09:07
                       Indirect
2:192.168.1.4:12::0::aa:bb:cc:80:d0:00::10.200.10.1/304 MAC/IP
                   *[EVPN/170] 09:44:46
                       Indirect
2:192.168.1.7:11::0::00:00:5e:00:01:01::10.200.20.254/304 MAC/IP
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 5021
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 5021
2:192.168.1.7:11::0::2c:6b:f5:fb:e9:f0::10.200.20.253/304 MAC/IP
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 5021
                       to 172.16.22.0 via ge-0/0/2.0, Push 5021
2:192.168.1.7:11::0::aa:bb:cc:80:f0:00::10.200.20.1/304 MAC/IP
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::00:00:5e:00:01:01::10.200.20.254/304 MAC/IP
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.12.0 via ge-0/0/1.0, Push 313
                       to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::2c:6b:f5:cd:68:f0::10.200.20.252/304 MAC/IP
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::aa:bb:cc:80:f0:00::10.200.20.1/304 MAC/IP
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.22.0 via ge-0/0/2.0, Push 313
3:192.168.1.3:12::0::192.168.1.3/248 IM
                   *[BGP/170] 10:05:39, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
3:192.168.1.4:12::0::192.168.1.4/248 IM
                   *[EVPN/170] 10:09:06
                       Indirect
3:192.168.1.7:11::0::192.168.1.7/248 IM
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
3:192.168.1.8:11::0::192.168.1.8/248 IM
                   *[BGP/170] 01:10:07, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.12.0 via ge-0/0/1.0
                    >  to 172.16.22.0 via ge-0/0/2.0
```

### SPINE-B1
```
root@SPINE-B1> show route

inet.0: 14 destinations, 28 routes (14 active, 0 holddown, 3 hidden)
+ = Active Route, - = Last Active, * = Both

100.2.1.0/31       *[Direct/0] 3d 10:35:59
                    >  via ge-0/0/9.0
100.2.1.1/32       *[Local/0] 3d 10:35:59
                       Local via ge-0/0/9.0
172.16.31.0/31     *[Direct/0] 2d 12:24:29
                    >  via ge-0/0/1.0
172.16.31.0/32     *[Local/0] 2d 12:24:29
                       Local via ge-0/0/1.0
172.16.32.0/31     *[Direct/0] 2d 12:24:29
                    >  via ge-0/0/2.0
172.16.32.0/32     *[Local/0] 2d 12:24:29
                       Local via ge-0/0/2.0
192.168.1.1/32     *[BGP/170] 00:56:00, localpref 150
                      AS path: 64512 65001 I, validation-state: unverified
                    >  to 100.2.1.0 via ge-0/0/9.0
                    [BGP/170] 01:02:15, localpref 100
                      AS path: 65007 65006 64512 65001 I, validation-state: unverified
                    >  to 172.16.31.1 via ge-0/0/1.0
                    [BGP/170] 00:56:00, localpref 100
                      AS path: 65008 65006 64512 65001 I, validation-state: unverified
                    >  to 172.16.32.1 via ge-0/0/2.0
192.168.1.2/32     *[BGP/170] 00:56:00, localpref 150
                      AS path: 64512 65002 I, validation-state: unverified
                    >  to 100.2.1.0 via ge-0/0/9.0
                    [BGP/170] 01:02:15, localpref 100
                      AS path: 65007 65006 64512 65002 I, validation-state: unverified
                    >  to 172.16.31.1 via ge-0/0/1.0
                    [BGP/170] 00:56:00, localpref 100
                      AS path: 65008 65006 64512 65002 I, validation-state: unverified
                    >  to 172.16.32.1 via ge-0/0/2.0
192.168.1.3/32     *[BGP/170] 00:56:00, localpref 150
                      AS path: 64512 65001 65003 I, validation-state: unverified
                    >  to 100.2.1.0 via ge-0/0/9.0
                    [BGP/170] 01:02:15, localpref 100
                      AS path: 65007 65006 64512 65001 65003 I, validation-state: unverified
                    >  to 172.16.31.1 via ge-0/0/1.0
                    [BGP/170] 00:56:00, localpref 100
                      AS path: 65008 65006 64512 65001 65003 I, validation-state: unverified
                    >  to 172.16.32.1 via ge-0/0/2.0
192.168.1.4/32     *[BGP/170] 00:56:00, localpref 150
                      AS path: 64512 65001 65004 I, validation-state: unverified
                    >  to 100.2.1.0 via ge-0/0/9.0
                    [BGP/170] 01:02:15, localpref 100
                      AS path: 65007 65006 64512 65001 65004 I, validation-state: unverified
                    >  to 172.16.31.1 via ge-0/0/1.0
                    [BGP/170] 00:56:00, localpref 100
                      AS path: 65008 65006 64512 65001 65004 I, validation-state: unverified
                    >  to 172.16.32.1 via ge-0/0/2.0
192.168.1.5/32     *[Direct/0] 3d 08:55:33
                    >  via lo0.0
192.168.1.6/32     *[BGP/170] 01:14:40, localpref 100
                      AS path: 65008 65006 I, validation-state: unverified
                       to 172.16.31.1 via ge-0/0/1.0
                    >  to 172.16.32.1 via ge-0/0/2.0
                    [BGP/170] 01:14:40, localpref 100
                      AS path: 65007 65006 I, validation-state: unverified
                    >  to 172.16.31.1 via ge-0/0/1.0
192.168.1.7/32     *[BGP/170] 01:14:40, localpref 100
                      AS path: 65007 I, validation-state: unverified
                    >  to 172.16.31.1 via ge-0/0/1.0
                    [BGP/170] 01:14:40, localpref 100
                      AS path: 65008 65006 65007 I, validation-state: unverified
                    >  to 172.16.32.1 via ge-0/0/2.0
192.168.1.8/32     *[BGP/170] 01:14:40, localpref 100
                      AS path: 65008 I, validation-state: unverified
                    >  to 172.16.32.1 via ge-0/0/2.0
                    [BGP/170] 01:14:40, localpref 100
                      AS path: 65007 65006 65008 I, validation-state: unverified
                    >  to 172.16.31.1 via ge-0/0/1.0

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe06:0/128
                   *[Local/0] 3d 21:06:10
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 3d 21:06:21
                       MultiRecv
```

### SPINE-B2
```
root@SPINE-B2> show route

inet.0: 14 destinations, 16 routes (14 active, 0 holddown, 1 hidden)
+ = Active Route, - = Last Active, * = Both

100.2.2.0/31       *[Direct/0] 2d 12:20:51
                    >  via ge-0/0/8.0
100.2.2.1/32       *[Local/0] 2d 12:20:51
                       Local via ge-0/0/8.0
172.16.41.0/31     *[Direct/0] 2d 12:24:59
                    >  via ge-0/0/1.0
172.16.41.0/32     *[Local/0] 2d 12:24:59
                       Local via ge-0/0/1.0
172.16.42.0/31     *[Direct/0] 2d 12:24:59
                    >  via ge-0/0/2.0
172.16.42.0/32     *[Local/0] 2d 12:24:59
                       Local via ge-0/0/2.0
192.168.1.1/32     *[BGP/170] 01:03:27, localpref 150
                      AS path: 64512 65001 I, validation-state: unverified
                    >  to 100.2.2.0 via ge-0/0/8.0
192.168.1.2/32     *[BGP/170] 01:03:27, localpref 150
                      AS path: 64512 65002 I, validation-state: unverified
                    >  to 100.2.2.0 via ge-0/0/8.0
192.168.1.3/32     *[BGP/170] 01:03:27, localpref 150
                      AS path: 64512 65001 65003 I, validation-state: unverified
                    >  to 100.2.2.0 via ge-0/0/8.0
192.168.1.4/32     *[BGP/170] 01:03:27, localpref 150
                      AS path: 64512 65001 65004 I, validation-state: unverified
                    >  to 100.2.2.0 via ge-0/0/8.0
192.168.1.5/32     *[BGP/170] 01:15:11, localpref 100, from 172.16.41.1
                      AS path: 65007 65005 I, validation-state: unverified
                       to 172.16.41.1 via ge-0/0/1.0
                    >  to 172.16.42.1 via ge-0/0/2.0
                    [BGP/170] 01:15:11, localpref 100
                      AS path: 65008 65005 I, validation-state: unverified
                    >  to 172.16.42.1 via ge-0/0/2.0
192.168.1.6/32     *[Direct/0] 2d 12:26:21
                    >  via lo0.0
192.168.1.7/32     *[BGP/170] 01:15:18, localpref 100
                      AS path: 65007 I, validation-state: unverified
                    >  to 172.16.41.1 via ge-0/0/1.0
192.168.1.8/32     *[BGP/170] 01:15:18, localpref 100
                      AS path: 65008 I, validation-state: unverified
                    >  to 172.16.42.1 via ge-0/0/2.0

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe07:0/128
                   *[Local/0] 2d 12:31:37
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 2d 12:31:48
                       MultiRecv
```

### LEAF-B1
```
root@LEAF-B1> show route | no-more

inet.0: 12 destinations, 18 routes (12 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

172.16.31.0/31     *[Direct/0] 1d 10:51:01
                    >  via ge-0/0/1.0
172.16.31.1/32     *[Local/0] 1d 10:51:01
                       Local via ge-0/0/1.0
172.16.41.0/31     *[Direct/0] 1d 10:51:01
                    >  via ge-0/0/2.0
172.16.41.1/32     *[Local/0] 1d 10:51:01
                       Local via ge-0/0/2.0
192.168.1.1/32     *[BGP/170] 00:56:56, localpref 100
                      AS path: 65006 64512 65001 I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
                    [BGP/170] 00:56:56, localpref 100
                      AS path: 65005 64512 65001 I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
192.168.1.2/32     *[BGP/170] 00:56:56, localpref 100
                      AS path: 65006 64512 65002 I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
                    [BGP/170] 00:56:56, localpref 100
                      AS path: 65005 64512 65002 I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
192.168.1.3/32     *[BGP/170] 00:56:56, localpref 100
                      AS path: 65006 64512 65001 65003 I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
                    [BGP/170] 00:56:56, localpref 100
                      AS path: 65005 64512 65001 65003 I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
192.168.1.4/32     *[BGP/170] 00:56:56, localpref 100
                      AS path: 65006 64512 65001 65004 I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
                    [BGP/170] 00:56:56, localpref 100
                      AS path: 65005 64512 65001 65004 I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
192.168.1.5/32     *[BGP/170] 01:15:37, localpref 100
                      AS path: 65005 I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
192.168.1.6/32     *[BGP/170] 01:15:43, localpref 100
                      AS path: 65006 I, validation-state: unverified
                    >  to 172.16.41.0 via ge-0/0/2.0
                    [BGP/170] 01:15:37, localpref 100
                      AS path: 65005 65008 65006 I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
192.168.1.7/32     *[Direct/0] 1d 10:51:01
                    >  via lo0.0
192.168.1.8/32     *[BGP/170] 01:15:37, localpref 100, from 172.16.41.0
                      AS path: 65006 65008 I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
                    [BGP/170] 01:15:37, localpref 100
                      AS path: 65005 65008 I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0

RED-L3PVN-VRF.inet.0: 4 destinations, 6 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.100.10.0/24     *[EVPN/170] 01:11:41
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
                    [EVPN/170] 01:11:41
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
10.100.20.0/24     *[Direct/0] 10:42:02
                    >  via irb.10
                    [EVPN/170] 01:15:48
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
10.100.20.1/32     *[EVPN/7] 01:15:48
                    >  via irb.10
10.100.20.253/32   *[Local/0] 10:42:02
                       Local via irb.10

GREEN-L3PVN-VRF.inet.0: 4 destinations, 6 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.200.10.0/24     *[EVPN/170] 01:11:41
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
                    [EVPN/170] 01:11:41
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
10.200.20.0/24     *[Direct/0] 11:53:39
                    >  via irb.20
                    [EVPN/170] 01:15:48
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
10.200.20.1/32     *[EVPN/7] 01:15:48
                    >  via irb.20
10.200.20.253/32   *[Local/0] 11:53:39
                       Local via irb.20

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe0a:0/128
                   *[Local/0] 1d 11:59:05
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 1d 11:59:16
                       MultiRecv

bgp.evpn.0: 96 destinations, 96 routes (96 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.3:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.3:0::050000fdeb0000139200::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.3:0::050000fdeb0000139c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.3:9::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
1:192.168.1.3:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
1:192.168.1.4:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.4:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.4:0::050000fdec0000139200::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.4:0::050000fdec0000139c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.4:9::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5010
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5010
1:192.168.1.4:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5020
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5020
1:192.168.1.7:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 10:04:50
                       Indirect
1:192.168.1.7:0::020000000000000002::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 10:04:50
                       Indirect
1:192.168.1.7:0::050000fdef0000139300::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 10:05:06
                       Indirect
1:192.168.1.7:0::050000fdef0000139d00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 11:53:39
                       Indirect
1:192.168.1.7:11::020000000000000002::0/192 AD/EVI
                   *[EVPN/170] 10:05:01
                       Indirect
1:192.168.1.7:12::020000000000000001::0/192 AD/EVI
                   *[EVPN/170] 10:05:01
                       Indirect
1:192.168.1.8:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:15:48, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.8:0::020000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:15:48, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.8:0::050000fdf00000139300::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:15:48, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.8:0::050000fdf00000139d00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:15:48, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.8:8::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:15:48, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5011
                       to 172.16.41.0 via ge-0/0/2.0, Push 5011
1:192.168.1.8:11::020000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:15:48, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 313
                       to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::2c:6b:f5:d2:9c:f0/304 MAC/IP
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::aa:bb:cc:00:c0:10/304 MAC/IP
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::2c:6b:f5:d2:9c:f0/304 MAC/IP
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::aa:bb:cc:00:d0:10/304 MAC/IP
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::aa:bb:cc:80:d0:00/304 MAC/IP
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::2c:6b:f5:fc:c8:f0/304 MAC/IP
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5010
                       to 172.16.41.0 via ge-0/0/2.0, Push 5010
2:192.168.1.4:9::0::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5010
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5010
2:192.168.1.4:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5020
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5020
2:192.168.1.4:12::0::2c:6b:f5:fc:c8:f0/304 MAC/IP
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5020
                       to 172.16.41.0 via ge-0/0/2.0, Push 5020
2:192.168.1.4:12::0::aa:bb:cc:80:d0:00/304 MAC/IP
                   *[BGP/170] 01:11:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 11:53:39
                       Indirect
2:192.168.1.7:11::0::2c:6b:f5:fb:e9:f0/304 MAC/IP
                   *[EVPN/170] 11:53:39
                       Indirect
2:192.168.1.7:11::0::aa:bb:cc:00:f0:10/304 MAC/IP
                   *[EVPN/170] 10:05:05
                       Indirect
2:192.168.1.7:11::0::aa:bb:cc:80:f0:00/304 MAC/IP
                   *[EVPN/170] 10:03:11
                       Indirect
2:192.168.1.7:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 10:05:06
                       Indirect
2:192.168.1.7:12::0::2c:6b:f5:fb:e9:f0/304 MAC/IP
                   *[EVPN/170] 10:05:06
                       Indirect
2:192.168.1.7:12::0::aa:bb:cc:00:e0:10/304 MAC/IP
                   *[EVPN/170] 10:05:06
                       Indirect
2:192.168.1.7:12::0::aa:bb:cc:80:e0:00/304 MAC/IP
                   *[EVPN/170] 10:05:06
                       Indirect
2:192.168.1.8:8::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:15:48, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5011
                       to 172.16.41.0 via ge-0/0/2.0, Push 5011
2:192.168.1.8:8::0::2c:6b:f5:cd:68:f0/304 MAC/IP
                   *[BGP/170] 01:15:48, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5011
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5011
2:192.168.1.8:8::0::aa:bb:cc:80:e0:00/304 MAC/IP
                   *[BGP/170] 01:15:48, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5011
                       to 172.16.41.0 via ge-0/0/2.0, Push 5011
2:192.168.1.8:11::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:15:48, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5021
                       to 172.16.41.0 via ge-0/0/2.0, Push 5021
2:192.168.1.8:11::0::2c:6b:f5:cd:68:f0/304 MAC/IP
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5021
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5021
2:192.168.1.8:11::0::aa:bb:cc:80:f0:00/304 MAC/IP
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 313
                       to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::00:00:5e:00:01:01::10.100.10.254/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::2c:6b:f5:d2:9c:f0::10.100.10.253/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::aa:bb:cc:80:c0:00::10.100.10.1/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 313
                       to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::00:00:5e:00:01:01::10.200.10.254/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 313
                       to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::2c:6b:f5:d2:9c:f0::10.200.10.253/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 313
                       to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::aa:bb:cc:80:d0:00::10.200.10.1/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::00:00:5e:00:01:01::10.100.10.254/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::2c:6b:f5:fc:c8:f0::10.100.10.252/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 313
                       to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::aa:bb:cc:80:c0:00::10.100.10.1/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5010
                       to 172.16.41.0 via ge-0/0/2.0, Push 5010
2:192.168.1.4:12::0::00:00:5e:00:01:01::10.200.10.254/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5020
                       to 172.16.41.0 via ge-0/0/2.0, Push 5020
2:192.168.1.4:12::0::2c:6b:f5:fc:c8:f0::10.200.10.252/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5020
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5020
2:192.168.1.4:12::0::aa:bb:cc:80:d0:00::10.200.10.1/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::00:00:5e:00:01:01::10.200.20.254/304 MAC/IP
                   *[EVPN/170] 11:53:40
                       Indirect
2:192.168.1.7:11::0::2c:6b:f5:fb:e9:f0::10.200.20.253/304 MAC/IP
                   *[EVPN/170] 11:53:40
                       Indirect
2:192.168.1.7:11::0::aa:bb:cc:80:f0:00::10.200.20.1/304 MAC/IP
                   *[EVPN/170] 10:03:12
                       Indirect
2:192.168.1.7:12::0::00:00:5e:00:01:01::10.100.20.254/304 MAC/IP
                   *[EVPN/170] 10:05:07
                       Indirect
2:192.168.1.7:12::0::2c:6b:f5:fb:e9:f0::10.100.20.253/304 MAC/IP
                   *[EVPN/170] 10:05:07
                       Indirect
2:192.168.1.7:12::0::aa:bb:cc:80:e0:00::10.100.20.1/304 MAC/IP
                   *[EVPN/170] 10:05:07
                       Indirect
2:192.168.1.8:8::0::00:00:5e:00:01:01::10.100.20.254/304 MAC/IP
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5011
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5011
2:192.168.1.8:8::0::2c:6b:f5:cd:68:f0::10.100.20.252/304 MAC/IP
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5011
                       to 172.16.41.0 via ge-0/0/2.0, Push 5011
2:192.168.1.8:8::0::aa:bb:cc:80:e0:00::10.100.20.1/304 MAC/IP
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5011
                       to 172.16.41.0 via ge-0/0/2.0, Push 5011
2:192.168.1.8:11::0::00:00:5e:00:01:01::10.200.20.254/304 MAC/IP
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5021
                       to 172.16.41.0 via ge-0/0/2.0, Push 5021
2:192.168.1.8:11::0::2c:6b:f5:cd:68:f0::10.200.20.252/304 MAC/IP
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5021
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5021
2:192.168.1.8:11::0::aa:bb:cc:80:f0:00::10.200.20.1/304 MAC/IP
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
3:192.168.1.3:9::0::192.168.1.3/248 IM
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
3:192.168.1.3:12::0::192.168.1.3/248 IM
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
3:192.168.1.4:9::0::192.168.1.4/248 IM
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
3:192.168.1.4:12::0::192.168.1.4/248 IM
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
3:192.168.1.7:11::0::192.168.1.7/248 IM
                   *[EVPN/170] 11:53:39
                       Indirect
3:192.168.1.7:12::0::192.168.1.7/248 IM
                   *[EVPN/170] 10:05:05
                       Indirect
3:192.168.1.8:8::0::192.168.1.8/248 IM
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
3:192.168.1.8:11::0::192.168.1.8/248 IM
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
4:192.168.1.7:0::020000000000000001:192.168.1.7/296 ES
                   *[EVPN/170] 10:04:52
                       Indirect
4:192.168.1.7:0::020000000000000002:192.168.1.7/296 ES
                   *[EVPN/170] 10:04:52
                       Indirect
4:192.168.1.8:0::020000000000000001:192.168.1.8/296 ES
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
4:192.168.1.8:0::020000000000000002:192.168.1.8/296 ES
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
5:192.168.1.3:10::0::10.100.10.0::24/248
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 318
5:192.168.1.3:11::0::10.200.10.0::24/248
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 325
                       to 172.16.41.0 via ge-0/0/2.0, Push 325
5:192.168.1.4:10::0::10.100.10.0::24/248
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5100
5:192.168.1.4:11::0::10.200.10.0::24/248
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5200
                       to 172.16.41.0 via ge-0/0/2.0, Push 5200
5:192.168.1.7:9::0::10.100.20.0::24/248
                   *[EVPN/170] 10:42:03
                       Fictitious
5:192.168.1.7:10::0::10.200.20.0::24/248
                   *[EVPN/170] 11:53:40
                       Fictitious
5:192.168.1.8:9::0::10.100.20.0::24/248
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5100
5:192.168.1.8:10::0::10.200.20.0::24/248
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5200
                       to 172.16.41.0 via ge-0/0/2.0, Push 5200

RED-VLAN-BASED-EVI.evpn.0: 40 destinations, 40 routes (40 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.3:0::050000fdeb0000139200::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.3:9::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
1:192.168.1.4:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.4:0::050000fdec0000139200::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.4:9::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5010
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5010
1:192.168.1.7:12::020000000000000001::0/192 AD/EVI
                   *[EVPN/170] 10:05:02
                       Indirect
1:192.168.1.8:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.8:0::050000fdf00000139300::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.8:8::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5011
                       to 172.16.41.0 via ge-0/0/2.0, Push 5011
2:192.168.1.3:9::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::2c:6b:f5:d2:9c:f0/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::aa:bb:cc:00:c0:10/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::2c:6b:f5:fc:c8:f0/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5010
                       to 172.16.41.0 via ge-0/0/2.0, Push 5010
2:192.168.1.4:9::0::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5010
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5010
2:192.168.1.7:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 10:05:07
                       Indirect
2:192.168.1.7:12::0::2c:6b:f5:fb:e9:f0/304 MAC/IP
                   *[EVPN/170] 10:05:07
                       Indirect
2:192.168.1.7:12::0::aa:bb:cc:00:e0:10/304 MAC/IP
                   *[EVPN/170] 10:05:07
                       Indirect
2:192.168.1.7:12::0::aa:bb:cc:80:e0:00/304 MAC/IP
                   *[EVPN/170] 10:05:07
                       Indirect
2:192.168.1.8:8::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5011
                       to 172.16.41.0 via ge-0/0/2.0, Push 5011
2:192.168.1.8:8::0::2c:6b:f5:cd:68:f0/304 MAC/IP
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5011
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5011
2:192.168.1.8:8::0::aa:bb:cc:80:e0:00/304 MAC/IP
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5011
                       to 172.16.41.0 via ge-0/0/2.0, Push 5011
2:192.168.1.3:9::0::00:00:5e:00:01:01::10.100.10.254/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::2c:6b:f5:d2:9c:f0::10.100.10.253/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::aa:bb:cc:80:c0:00::10.100.10.1/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 313
                       to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::00:00:5e:00:01:01::10.100.10.254/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::2c:6b:f5:fc:c8:f0::10.100.10.252/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 313
                       to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::aa:bb:cc:80:c0:00::10.100.10.1/304 MAC/IP
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5010
                       to 172.16.41.0 via ge-0/0/2.0, Push 5010
2:192.168.1.7:12::0::00:00:5e:00:01:01::10.100.20.254/304 MAC/IP
                   *[EVPN/170] 10:05:07
                       Indirect
2:192.168.1.7:12::0::2c:6b:f5:fb:e9:f0::10.100.20.253/304 MAC/IP
                   *[EVPN/170] 10:05:07
                       Indirect
2:192.168.1.7:12::0::aa:bb:cc:80:e0:00::10.100.20.1/304 MAC/IP
                   *[EVPN/170] 10:05:07
                       Indirect
2:192.168.1.8:8::0::00:00:5e:00:01:01::10.100.20.254/304 MAC/IP
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5011
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5011
2:192.168.1.8:8::0::2c:6b:f5:cd:68:f0::10.100.20.252/304 MAC/IP
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5011
                       to 172.16.41.0 via ge-0/0/2.0, Push 5011
2:192.168.1.8:8::0::aa:bb:cc:80:e0:00::10.100.20.1/304 MAC/IP
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5011
                       to 172.16.41.0 via ge-0/0/2.0, Push 5011
3:192.168.1.3:9::0::192.168.1.3/248 IM
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
3:192.168.1.4:9::0::192.168.1.4/248 IM
                   *[BGP/170] 01:11:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
3:192.168.1.7:12::0::192.168.1.7/248 IM
                   *[EVPN/170] 10:05:05
                       Indirect
3:192.168.1.8:8::0::192.168.1.8/248 IM
                   *[BGP/170] 01:15:49, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0

__default_evpn__.evpn.0: 8 destinations, 8 routes (8 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.7:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 10:04:52
                       Indirect
1:192.168.1.7:0::020000000000000002::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 10:04:52
                       Indirect
1:192.168.1.7:0::050000fdef0000139300::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 10:05:08
                       Indirect
1:192.168.1.7:0::050000fdef0000139d00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 11:53:41
                       Indirect
4:192.168.1.7:0::020000000000000001:192.168.1.7/296 ES
                   *[EVPN/170] 10:04:53
                       Indirect
4:192.168.1.7:0::020000000000000002:192.168.1.7/296 ES
                   *[EVPN/170] 10:04:53
                       Indirect
4:192.168.1.8:0::020000000000000001:192.168.1.8/296 ES
                   *[BGP/170] 01:15:50, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
4:192.168.1.8:0::020000000000000002:192.168.1.8/296 ES
                   *[BGP/170] 01:15:50, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0

RED-L3PVN-VRF.evpn.0: 4 destinations, 4 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

5:192.168.1.3:10::0::10.100.10.0::24/248
                   *[BGP/170] 01:11:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 318
5:192.168.1.4:10::0::10.100.10.0::24/248
                   *[BGP/170] 01:11:43, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5100
5:192.168.1.7:9::0::10.100.20.0::24/248
                   *[EVPN/170] 10:42:04
                       Fictitious
5:192.168.1.8:9::0::10.100.20.0::24/248
                   *[BGP/170] 01:15:50, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5100
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5100

GREEN-L3PVN-VRF.evpn.0: 4 destinations, 4 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

5:192.168.1.3:11::0::10.200.10.0::24/248
                   *[BGP/170] 01:11:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 325
                       to 172.16.41.0 via ge-0/0/2.0, Push 325
5:192.168.1.4:11::0::10.200.10.0::24/248
                   *[BGP/170] 01:11:43, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5200
                       to 172.16.41.0 via ge-0/0/2.0, Push 5200
5:192.168.1.7:10::0::10.200.20.0::24/248
                   *[EVPN/170] 11:53:41
                       Fictitious
5:192.168.1.8:10::0::10.200.20.0::24/248
                   *[BGP/170] 01:15:50, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5200
                       to 172.16.41.0 via ge-0/0/2.0, Push 5200

GREEN-VLAN-BASED-EVI.evpn.0: 40 destinations, 40 routes (40 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.3:0::050000fdeb0000139c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.3:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
1:192.168.1.4:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0
                       to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.4:0::050000fdec0000139c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.4:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5020
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5020
1:192.168.1.7:11::020000000000000002::0/192 AD/EVI
                   *[EVPN/170] 10:05:04
                       Indirect
1:192.168.1.8:0::020000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:15:51, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.8:0::050000fdf00000139d00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:15:51, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
1:192.168.1.8:11::020000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:15:51, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 313
                       to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::2c:6b:f5:d2:9c:f0/304 MAC/IP
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::aa:bb:cc:00:d0:10/304 MAC/IP
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::aa:bb:cc:80:d0:00/304 MAC/IP
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5020
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5020
2:192.168.1.4:12::0::2c:6b:f5:fc:c8:f0/304 MAC/IP
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5020
                       to 172.16.41.0 via ge-0/0/2.0, Push 5020
2:192.168.1.4:12::0::aa:bb:cc:80:d0:00/304 MAC/IP
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 11:53:42
                       Indirect
2:192.168.1.7:11::0::2c:6b:f5:fb:e9:f0/304 MAC/IP
                   *[EVPN/170] 11:53:42
                       Indirect
2:192.168.1.7:11::0::aa:bb:cc:00:f0:10/304 MAC/IP
                   *[EVPN/170] 10:05:08
                       Indirect
2:192.168.1.7:11::0::aa:bb:cc:80:f0:00/304 MAC/IP
                   *[EVPN/170] 10:03:14
                       Indirect
2:192.168.1.8:11::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:15:51, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5021
                       to 172.16.41.0 via ge-0/0/2.0, Push 5021
2:192.168.1.8:11::0::2c:6b:f5:cd:68:f0/304 MAC/IP
                   *[BGP/170] 01:15:51, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5021
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5021
2:192.168.1.8:11::0::aa:bb:cc:80:f0:00/304 MAC/IP
                   *[BGP/170] 01:15:51, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 313
                       to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::00:00:5e:00:01:01::10.200.10.254/304 MAC/IP
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 313
                       to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::2c:6b:f5:d2:9c:f0::10.200.10.253/304 MAC/IP
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 313
                       to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::aa:bb:cc:80:d0:00::10.200.10.1/304 MAC/IP
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:12::0::00:00:5e:00:01:01::10.200.10.254/304 MAC/IP
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5020
                       to 172.16.41.0 via ge-0/0/2.0, Push 5020
2:192.168.1.4:12::0::2c:6b:f5:fc:c8:f0::10.200.10.252/304 MAC/IP
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5020
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5020
2:192.168.1.4:12::0::aa:bb:cc:80:d0:00::10.200.10.1/304 MAC/IP
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::00:00:5e:00:01:01::10.200.20.254/304 MAC/IP
                   *[EVPN/170] 11:53:42
                       Indirect
2:192.168.1.7:11::0::2c:6b:f5:fb:e9:f0::10.200.20.253/304 MAC/IP
                   *[EVPN/170] 11:53:42
                       Indirect
2:192.168.1.7:11::0::aa:bb:cc:80:f0:00::10.200.20.1/304 MAC/IP
                   *[EVPN/170] 10:03:14
                       Indirect
2:192.168.1.8:11::0::00:00:5e:00:01:01::10.200.20.254/304 MAC/IP
                   *[BGP/170] 01:15:51, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                    >  to 172.16.31.0 via ge-0/0/1.0, Push 5021
                       to 172.16.41.0 via ge-0/0/2.0, Push 5021
2:192.168.1.8:11::0::2c:6b:f5:cd:68:f0::10.200.20.252/304 MAC/IP
                   *[BGP/170] 01:15:51, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 5021
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 5021
2:192.168.1.8:11::0::aa:bb:cc:80:f0:00::10.200.20.1/304 MAC/IP
                   *[BGP/170] 01:15:51, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.41.0 via ge-0/0/2.0, Push 313
3:192.168.1.3:12::0::192.168.1.3/248 IM
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
3:192.168.1.4:12::0::192.168.1.4/248 IM
                   *[BGP/170] 01:11:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
3:192.168.1.7:11::0::192.168.1.7/248 IM
                   *[EVPN/170] 11:53:41
                       Indirect
3:192.168.1.8:11::0::192.168.1.8/248 IM
                   *[BGP/170] 01:15:51, localpref 100, from 192.168.1.8
                      AS path: I, validation-state: unverified
                       to 172.16.31.0 via ge-0/0/1.0
                    >  to 172.16.41.0 via ge-0/0/2.0
```

### LEAF-B2
```
root@LEAF-B2> show route | no-more

inet.0: 12 destinations, 18 routes (12 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

172.16.32.0/31     *[Direct/0] 1d 10:46:03
                    >  via ge-0/0/1.0
172.16.32.1/32     *[Local/0] 1d 10:46:03
                       Local via ge-0/0/1.0
172.16.42.0/31     *[Direct/0] 1d 10:46:03
                    >  via ge-0/0/2.0
172.16.42.1/32     *[Local/0] 1d 10:46:03
                       Local via ge-0/0/2.0
192.168.1.1/32     *[BGP/170] 00:57:26, localpref 100
                      AS path: 65006 64512 65001 I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
                    [BGP/170] 00:57:26, localpref 100
                      AS path: 65005 64512 65001 I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
192.168.1.2/32     *[BGP/170] 00:57:26, localpref 100
                      AS path: 65006 64512 65002 I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
                    [BGP/170] 00:57:26, localpref 100
                      AS path: 65005 64512 65002 I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
192.168.1.3/32     *[BGP/170] 00:57:26, localpref 100
                      AS path: 65006 64512 65001 65003 I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
                    [BGP/170] 00:57:26, localpref 100
                      AS path: 65005 64512 65001 65003 I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
192.168.1.4/32     *[BGP/170] 00:57:26, localpref 100
                      AS path: 65006 64512 65001 65004 I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
                    [BGP/170] 00:57:26, localpref 100
                      AS path: 65005 64512 65001 65004 I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
192.168.1.5/32     *[BGP/170] 01:16:07, localpref 100
                      AS path: 65005 I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                    [BGP/170] 01:16:06, localpref 100
                      AS path: 65006 65007 65005 I, validation-state: unverified
                    >  to 172.16.42.0 via ge-0/0/2.0
192.168.1.6/32     *[BGP/170] 01:16:13, localpref 100
                      AS path: 65006 I, validation-state: unverified
                    >  to 172.16.42.0 via ge-0/0/2.0
192.168.1.7/32     *[BGP/170] 01:16:07, localpref 100
                      AS path: 65006 65007 I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
                    [BGP/170] 01:16:07, localpref 100
                      AS path: 65005 65007 I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
192.168.1.8/32     *[Direct/0] 1d 10:46:03
                    >  via lo0.0

RED-L3PVN-VRF.inet.0: 4 destinations, 6 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.100.10.0/24     *[EVPN/170] 01:12:41
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
                    [EVPN/170] 01:12:41
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
10.100.20.0/24     *[Direct/0] 1d 08:48:04
                    >  via irb.10
                    [EVPN/170] 01:16:18
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
10.100.20.1/32     *[EVPN/7] 01:16:18
                    >  via irb.10
10.100.20.252/32   *[Local/0] 1d 08:48:04
                       Local via irb.10

GREEN-L3PVN-VRF.inet.0: 4 destinations, 6 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

10.200.10.0/24     *[EVPN/170] 01:12:41
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
                    [EVPN/170] 01:12:41
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
10.200.20.0/24     *[Direct/0] 11:54:12
                    >  via irb.20
                    [EVPN/170] 01:16:18
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
10.200.20.1/32     *[EVPN/7] 01:16:18
                    >  via irb.20
10.200.20.252/32   *[Local/0] 11:54:12
                       Local via irb.20

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
Limit/Threshold: 1048576/1048576 destinations
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe0b:0/128
                   *[Local/0] 1d 11:59:22
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 1d 11:59:33
                       MultiRecv

bgp.evpn.0: 96 destinations, 96 routes (96 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.3:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.3:0::050000fdeb0000139200::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.3:0::050000fdeb0000139c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.3:9::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
1:192.168.1.3:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
1:192.168.1.4:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.4:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.4:0::050000fdec0000139200::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.4:0::050000fdec0000139c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.4:9::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
1:192.168.1.4:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
1:192.168.1.7:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:16:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.7:0::020000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:16:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.7:0::050000fdef0000139300::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:16:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.7:0::050000fdef0000139d00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:16:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.7:11::020000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:16:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
1:192.168.1.7:12::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:16:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
1:192.168.1.8:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 1d 09:11:30
                       Indirect
1:192.168.1.8:0::020000000000000002::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 10:05:22
                       Indirect
1:192.168.1.8:0::050000fdf00000139300::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 1d 08:48:03
                       Indirect
1:192.168.1.8:0::050000fdf00000139d00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 11:54:12
                       Indirect
1:192.168.1.8:8::020000000000000001::0/192 AD/EVI
                   *[EVPN/170] 1d 09:11:41
                       Indirect
1:192.168.1.8:11::020000000000000002::0/192 AD/EVI
                   *[EVPN/170] 10:05:33
                       Indirect
2:192.168.1.3:9::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::2c:6b:f5:d2:9c:f0/304 MAC/IP
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::aa:bb:cc:00:c0:10/304 MAC/IP
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::2c:6b:f5:d2:9c:f0/304 MAC/IP
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::aa:bb:cc:00:d0:10/304 MAC/IP
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::aa:bb:cc:80:d0:00/304 MAC/IP
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::2c:6b:f5:fc:c8:f0/304 MAC/IP
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:12::0::2c:6b:f5:fc:c8:f0/304 MAC/IP
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:12::0::aa:bb:cc:80:d0:00/304 MAC/IP
                   *[BGP/170] 01:12:41, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:16:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 5021
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 5021
2:192.168.1.7:11::0::2c:6b:f5:fb:e9:f0/304 MAC/IP
                   *[BGP/170] 01:16:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 5021
                       to 172.16.42.0 via ge-0/0/2.0, Push 5021
2:192.168.1.7:11::0::aa:bb:cc:00:f0:10/304 MAC/IP
                   *[BGP/170] 01:16:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::aa:bb:cc:80:f0:00/304 MAC/IP
                   *[BGP/170] 01:16:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:16:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::2c:6b:f5:fb:e9:f0/304 MAC/IP
                   *[BGP/170] 01:16:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::aa:bb:cc:00:e0:10/304 MAC/IP
                   *[BGP/170] 01:16:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::aa:bb:cc:80:e0:00/304 MAC/IP
                   *[BGP/170] 01:16:18, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 1d 08:48:03
                       Indirect
2:192.168.1.8:8::0::2c:6b:f5:cd:68:f0/304 MAC/IP
                   *[EVPN/170] 1d 08:48:03
                       Indirect
2:192.168.1.8:8::0::aa:bb:cc:80:e0:00/304 MAC/IP
                   *[EVPN/170] 10:41:57
                       Indirect
2:192.168.1.8:11::0::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 11:54:12
                       Indirect
2:192.168.1.8:11::0::2c:6b:f5:cd:68:f0/304 MAC/IP
                   *[EVPN/170] 11:54:13
                       Indirect
2:192.168.1.8:11::0::aa:bb:cc:80:f0:00/304 MAC/IP
                   *[EVPN/170] 10:03:41
                       Indirect
2:192.168.1.3:9::0::00:00:5e:00:01:01::10.100.10.254/304 MAC/IP
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::2c:6b:f5:d2:9c:f0::10.100.10.253/304 MAC/IP
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::aa:bb:cc:80:c0:00::10.100.10.1/304 MAC/IP
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::00:00:5e:00:01:01::10.200.10.254/304 MAC/IP
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::2c:6b:f5:d2:9c:f0::10.200.10.253/304 MAC/IP
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::aa:bb:cc:80:d0:00::10.200.10.1/304 MAC/IP
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::00:00:5e:00:01:01::10.100.10.254/304 MAC/IP
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::2c:6b:f5:fc:c8:f0::10.100.10.252/304 MAC/IP
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::aa:bb:cc:80:c0:00::10.100.10.1/304 MAC/IP
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:12::0::00:00:5e:00:01:01::10.200.10.254/304 MAC/IP
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:12::0::2c:6b:f5:fc:c8:f0::10.200.10.252/304 MAC/IP
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:12::0::aa:bb:cc:80:d0:00::10.200.10.1/304 MAC/IP
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::00:00:5e:00:01:01::10.200.20.254/304 MAC/IP
                   *[BGP/170] 01:16:19, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 5021
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 5021
2:192.168.1.7:11::0::2c:6b:f5:fb:e9:f0::10.200.20.253/304 MAC/IP
                   *[BGP/170] 01:16:19, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 5021
                       to 172.16.42.0 via ge-0/0/2.0, Push 5021
2:192.168.1.7:11::0::aa:bb:cc:80:f0:00::10.200.20.1/304 MAC/IP
                   *[BGP/170] 01:16:19, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::00:00:5e:00:01:01::10.100.20.254/304 MAC/IP
                   *[BGP/170] 01:16:19, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::2c:6b:f5:fb:e9:f0::10.100.20.253/304 MAC/IP
                   *[BGP/170] 01:16:19, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::aa:bb:cc:80:e0:00::10.100.20.1/304 MAC/IP
                   *[BGP/170] 01:16:19, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::00:00:5e:00:01:01::10.100.20.254/304 MAC/IP
                   *[EVPN/170] 1d 08:48:04
                       Indirect
2:192.168.1.8:8::0::2c:6b:f5:cd:68:f0::10.100.20.252/304 MAC/IP
                   *[EVPN/170] 1d 08:48:04
                       Indirect
2:192.168.1.8:8::0::aa:bb:cc:80:e0:00::10.100.20.1/304 MAC/IP
                   *[EVPN/170] 10:41:58
                       Indirect
2:192.168.1.8:11::0::00:00:5e:00:01:01::10.200.20.254/304 MAC/IP
                   *[EVPN/170] 11:54:13
                       Indirect
2:192.168.1.8:11::0::2c:6b:f5:cd:68:f0::10.200.20.252/304 MAC/IP
                   *[EVPN/170] 11:54:13
                       Indirect
2:192.168.1.8:11::0::aa:bb:cc:80:f0:00::10.200.20.1/304 MAC/IP
                   *[EVPN/170] 10:03:41
                       Indirect
3:192.168.1.3:9::0::192.168.1.3/248 IM
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
3:192.168.1.3:12::0::192.168.1.3/248 IM
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
3:192.168.1.4:9::0::192.168.1.4/248 IM
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
3:192.168.1.4:12::0::192.168.1.4/248 IM
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
3:192.168.1.7:11::0::192.168.1.7/248 IM
                   *[BGP/170] 01:16:19, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
3:192.168.1.7:12::0::192.168.1.7/248 IM
                   *[BGP/170] 01:16:19, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
3:192.168.1.8:8::0::192.168.1.8/248 IM
                   *[EVPN/170] 1d 09:14:54
                       Indirect
3:192.168.1.8:11::0::192.168.1.8/248 IM
                   *[EVPN/170] 11:54:12
                       Indirect
4:192.168.1.7:0::020000000000000001:192.168.1.7/296 ES
                   *[BGP/170] 01:16:19, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
4:192.168.1.7:0::020000000000000002:192.168.1.7/296 ES
                   *[BGP/170] 01:16:19, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
4:192.168.1.8:0::020000000000000001:192.168.1.8/296 ES
                   *[EVPN/170] 1d 09:11:32
                       Indirect
4:192.168.1.8:0::020000000000000002:192.168.1.8/296 ES
                   *[EVPN/170] 10:05:24
                       Indirect
5:192.168.1.3:10::0::10.100.10.0::24/248
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 318
5:192.168.1.3:11::0::10.200.10.0::24/248
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 325
                       to 172.16.42.0 via ge-0/0/2.0, Push 325
5:192.168.1.4:10::0::10.100.10.0::24/248
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 318
5:192.168.1.4:11::0::10.200.10.0::24/248
                   *[BGP/170] 01:12:42, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 325
                       to 172.16.42.0 via ge-0/0/2.0, Push 325
5:192.168.1.7:9::0::10.100.20.0::24/248
                   *[BGP/170] 01:16:19, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 318
                       to 172.16.42.0 via ge-0/0/2.0, Push 318
5:192.168.1.7:10::0::10.200.20.0::24/248
                   *[BGP/170] 01:16:19, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 325
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 325
5:192.168.1.8:9::0::10.100.20.0::24/248
                   *[EVPN/170] 1d 08:48:05
                       Fictitious
5:192.168.1.8:10::0::10.200.20.0::24/248
                   *[EVPN/170] 11:54:13
                       Fictitious

RED-VLAN-BASED-EVI.evpn.0: 40 destinations, 40 routes (40 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.3:0::050000fdeb0000139200::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.3:9::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
1:192.168.1.4:0::010000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.4:0::050000fdec0000139200::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.4:9::010000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
1:192.168.1.7:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:16:20, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.7:0::050000fdef0000139300::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:16:20, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.7:12::020000000000000001::0/192 AD/EVI
                   *[BGP/170] 01:16:20, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
1:192.168.1.8:8::020000000000000001::0/192 AD/EVI
                   *[EVPN/170] 1d 09:11:43
                       Indirect
2:192.168.1.3:9::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::2c:6b:f5:d2:9c:f0/304 MAC/IP
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::aa:bb:cc:00:c0:10/304 MAC/IP
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::2c:6b:f5:fc:c8:f0/304 MAC/IP
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::aa:bb:cc:80:c0:00/304 MAC/IP
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:16:20, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::2c:6b:f5:fb:e9:f0/304 MAC/IP
                   *[BGP/170] 01:16:20, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::aa:bb:cc:00:e0:10/304 MAC/IP
                   *[BGP/170] 01:16:20, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::aa:bb:cc:80:e0:00/304 MAC/IP
                   *[BGP/170] 01:16:20, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 1d 08:48:05
                       Indirect
2:192.168.1.8:8::0::2c:6b:f5:cd:68:f0/304 MAC/IP
                   *[EVPN/170] 1d 08:48:05
                       Indirect
2:192.168.1.8:8::0::aa:bb:cc:80:e0:00/304 MAC/IP
                   *[EVPN/170] 10:41:59
                       Indirect
2:192.168.1.3:9::0::00:00:5e:00:01:01::10.100.10.254/304 MAC/IP
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::2c:6b:f5:d2:9c:f0::10.100.10.253/304 MAC/IP
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:9::0::aa:bb:cc:80:c0:00::10.100.10.1/304 MAC/IP
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::00:00:5e:00:01:01::10.100.10.254/304 MAC/IP
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::2c:6b:f5:fc:c8:f0::10.100.10.252/304 MAC/IP
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:9::0::aa:bb:cc:80:c0:00::10.100.10.1/304 MAC/IP
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::00:00:5e:00:01:01::10.100.20.254/304 MAC/IP
                   *[BGP/170] 01:16:20, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::2c:6b:f5:fb:e9:f0::10.100.20.253/304 MAC/IP
                   *[BGP/170] 01:16:20, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:12::0::aa:bb:cc:80:e0:00::10.100.20.1/304 MAC/IP
                   *[BGP/170] 01:16:20, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:8::0::00:00:5e:00:01:01::10.100.20.254/304 MAC/IP
                   *[EVPN/170] 1d 08:48:05
                       Indirect
2:192.168.1.8:8::0::2c:6b:f5:cd:68:f0::10.100.20.252/304 MAC/IP
                   *[EVPN/170] 1d 08:48:05
                       Indirect
2:192.168.1.8:8::0::aa:bb:cc:80:e0:00::10.100.20.1/304 MAC/IP
                   *[EVPN/170] 10:41:59
                       Indirect
3:192.168.1.3:9::0::192.168.1.3/248 IM
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
3:192.168.1.4:9::0::192.168.1.4/248 IM
                   *[BGP/170] 01:12:43, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
3:192.168.1.7:12::0::192.168.1.7/248 IM
                   *[BGP/170] 01:16:20, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
3:192.168.1.8:8::0::192.168.1.8/248 IM
                   *[EVPN/170] 1d 09:14:55
                       Indirect

__default_evpn__.evpn.0: 8 destinations, 8 routes (8 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.8:0::020000000000000001::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 1d 09:11:33
                       Indirect
1:192.168.1.8:0::020000000000000002::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 10:05:25
                       Indirect
1:192.168.1.8:0::050000fdf00000139300::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 1d 08:48:06
                       Indirect
1:192.168.1.8:0::050000fdf00000139d00::FFFF:FFFF/192 AD/ESI
                   *[EVPN/170] 11:54:15
                       Indirect
4:192.168.1.7:0::020000000000000001:192.168.1.7/296 ES
                   *[BGP/170] 01:16:21, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
4:192.168.1.7:0::020000000000000002:192.168.1.7/296 ES
                   *[BGP/170] 01:16:21, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
4:192.168.1.8:0::020000000000000001:192.168.1.8/296 ES
                   *[EVPN/170] 1d 09:11:34
                       Indirect
4:192.168.1.8:0::020000000000000002:192.168.1.8/296 ES
                   *[EVPN/170] 10:05:26
                       Indirect

RED-L3PVN-VRF.evpn.0: 4 destinations, 4 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

5:192.168.1.3:10::0::10.100.10.0::24/248
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 318
5:192.168.1.4:10::0::10.100.10.0::24/248
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 318
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 318
5:192.168.1.7:9::0::10.100.20.0::24/248
                   *[BGP/170] 01:16:21, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 318
                       to 172.16.42.0 via ge-0/0/2.0, Push 318
5:192.168.1.8:9::0::10.100.20.0::24/248
                   *[EVPN/170] 1d 08:48:07
                       Fictitious

GREEN-L3PVN-VRF.evpn.0: 4 destinations, 4 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

5:192.168.1.3:11::0::10.200.10.0::24/248
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 325
                       to 172.16.42.0 via ge-0/0/2.0, Push 325
5:192.168.1.4:11::0::10.200.10.0::24/248
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 325
                       to 172.16.42.0 via ge-0/0/2.0, Push 325
5:192.168.1.7:10::0::10.200.20.0::24/248
                   *[BGP/170] 01:16:21, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 325
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 325
5:192.168.1.8:10::0::10.200.20.0::24/248
                   *[EVPN/170] 11:54:15
                       Fictitious

GREEN-VLAN-BASED-EVI.evpn.0: 40 destinations, 40 routes (40 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

1:192.168.1.3:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.3:0::050000fdeb0000139c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.3:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
1:192.168.1.4:0::010000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.4:0::050000fdec0000139c00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.4:12::010000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
1:192.168.1.7:0::020000000000000002::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:16:21, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0
                       to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.7:0::050000fdef0000139d00::FFFF:FFFF/192 AD/ESI
                   *[BGP/170] 01:16:21, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
1:192.168.1.7:11::020000000000000002::0/192 AD/EVI
                   *[BGP/170] 01:16:21, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
1:192.168.1.8:11::020000000000000002::0/192 AD/EVI
                   *[EVPN/170] 10:05:36
                       Indirect
2:192.168.1.3:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::2c:6b:f5:d2:9c:f0/304 MAC/IP
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::aa:bb:cc:00:d0:10/304 MAC/IP
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::aa:bb:cc:80:d0:00/304 MAC/IP
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:12::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:12::0::2c:6b:f5:fc:c8:f0/304 MAC/IP
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:12::0::aa:bb:cc:80:d0:00/304 MAC/IP
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::00:00:5e:00:01:01/304 MAC/IP
                   *[BGP/170] 01:16:21, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 5021
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 5021
2:192.168.1.7:11::0::2c:6b:f5:fb:e9:f0/304 MAC/IP
                   *[BGP/170] 01:16:21, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 5021
                       to 172.16.42.0 via ge-0/0/2.0, Push 5021
2:192.168.1.7:11::0::aa:bb:cc:00:f0:10/304 MAC/IP
                   *[BGP/170] 01:16:21, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::aa:bb:cc:80:f0:00/304 MAC/IP
                   *[BGP/170] 01:16:21, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::00:00:5e:00:01:01/304 MAC/IP
                   *[EVPN/170] 11:54:15
                       Indirect
2:192.168.1.8:11::0::2c:6b:f5:cd:68:f0/304 MAC/IP
                   *[EVPN/170] 11:54:15
                       Indirect
2:192.168.1.8:11::0::aa:bb:cc:80:f0:00/304 MAC/IP
                   *[EVPN/170] 10:03:43
                       Indirect
2:192.168.1.3:12::0::00:00:5e:00:01:01::10.200.10.254/304 MAC/IP
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::2c:6b:f5:d2:9c:f0::10.200.10.253/304 MAC/IP
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.3:12::0::aa:bb:cc:80:d0:00::10.200.10.1/304 MAC/IP
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:12::0::00:00:5e:00:01:01::10.200.10.254/304 MAC/IP
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:12::0::2c:6b:f5:fc:c8:f0::10.200.10.252/304 MAC/IP
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.4:12::0::aa:bb:cc:80:d0:00::10.200.10.1/304 MAC/IP
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 313
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.7:11::0::00:00:5e:00:01:01::10.200.20.254/304 MAC/IP
                   *[BGP/170] 01:16:21, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0, Push 5021
                    >  to 172.16.42.0 via ge-0/0/2.0, Push 5021
2:192.168.1.7:11::0::2c:6b:f5:fb:e9:f0::10.200.20.253/304 MAC/IP
                   *[BGP/170] 01:16:21, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 5021
                       to 172.16.42.0 via ge-0/0/2.0, Push 5021
2:192.168.1.7:11::0::aa:bb:cc:80:f0:00::10.200.20.1/304 MAC/IP
                   *[BGP/170] 01:16:21, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                    >  to 172.16.32.0 via ge-0/0/1.0, Push 313
                       to 172.16.42.0 via ge-0/0/2.0, Push 313
2:192.168.1.8:11::0::00:00:5e:00:01:01::10.200.20.254/304 MAC/IP
                   *[EVPN/170] 11:54:15
                       Indirect
2:192.168.1.8:11::0::2c:6b:f5:cd:68:f0::10.200.20.252/304 MAC/IP
                   *[EVPN/170] 11:54:15
                       Indirect
2:192.168.1.8:11::0::aa:bb:cc:80:f0:00::10.200.20.1/304 MAC/IP
                   *[EVPN/170] 10:03:43
                       Indirect
3:192.168.1.3:12::0::192.168.1.3/248 IM
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.3
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
3:192.168.1.4:12::0::192.168.1.4/248 IM
                   *[BGP/170] 01:12:44, localpref 100, from 192.168.1.4
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
3:192.168.1.7:11::0::192.168.1.7/248 IM
                   *[BGP/170] 01:16:21, localpref 100, from 192.168.1.7
                      AS path: I, validation-state: unverified
                       to 172.16.32.0 via ge-0/0/1.0
                    >  to 172.16.42.0 via ge-0/0/2.0
3:192.168.1.8:11::0::192.168.1.8/248 IM
                   *[EVPN/170] 11:54:14
                       Indirect
```

### PE1
```
root@PE1> show route

inet.0: 8 destinations, 8 routes (8 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

100.0.1.0/31       *[Direct/0] 3d 10:40:57
                    >  via ge-0/0/1.0
100.0.1.1/32       *[Local/0] 3d 10:40:57
                       Local via ge-0/0/1.0
100.0.2.0/31       *[OSPF/10] 3d 10:40:57, metric 200
                    >  to 100.0.1.0 via ge-0/0/1.0
192.168.255.1/32   *[Direct/0] 3d 21:00:41
                    >  via lo0.0
192.168.255.2/32   *[OSPF/10] 3d 10:40:57, metric 100
                    >  to 100.0.1.0 via ge-0/0/1.0
192.168.255.3/32   *[OSPF/10] 3d 10:40:57, metric 200
                    >  to 100.0.1.0 via ge-0/0/1.0
224.0.0.2/32       *[LDP/9] 3d 20:57:52, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 3d 20:55:59, metric 1
                       MultiRecv

inet.3: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.255.2/32   *[LDP/9] 3d 10:40:56, metric 1
                    >  to 100.0.1.0 via ge-0/0/1.0
192.168.255.3/32   *[LDP/9] 3d 10:40:56, metric 1
                    >  to 100.0.1.0 via ge-0/0/1.0, Push 299776

DC-LLC_VRF.inet.0: 12 destinations, 16 routes (12 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

100.1.1.0/31       *[Direct/0] 3d 09:12:04
                    >  via ge-0/0/9.0
100.1.1.0/32       *[Local/0] 3d 09:12:04
                       Local via ge-0/0/9.0
100.1.2.0/31       *[Direct/0] 3d 08:11:42
                    >  via ge-0/0/8.0
100.1.2.0/32       *[Local/0] 3d 08:11:42
                       Local via ge-0/0/8.0
192.168.1.1/32     *[BGP/170] 2d 11:23:31, localpref 100
                      AS path: 65001 I, validation-state: unverified
                    >  to 100.1.1.1 via ge-0/0/9.0
                    [BGP/170] 03:14:16, localpref 100
                      AS path: 65002 65003 65001 I, validation-state: unverified
                    >  to 100.1.2.1 via ge-0/0/8.0
192.168.1.2/32     *[BGP/170] 2d 09:07:15, localpref 100
                      AS path: 65002 I, validation-state: unverified
                    >  to 100.1.2.1 via ge-0/0/8.0
                    [BGP/170] 03:16:18, localpref 100
                      AS path: 65001 65003 65002 I, validation-state: unverified
                    >  to 100.1.1.1 via ge-0/0/9.0
192.168.1.3/32     *[BGP/170] 03:16:18, localpref 100
                      AS path: 65001 65003 I, validation-state: unverified
                    >  to 100.1.1.1 via ge-0/0/9.0
                    [BGP/170] 03:14:16, localpref 100
                      AS path: 65002 65003 I, validation-state: unverified
                    >  to 100.1.2.1 via ge-0/0/8.0
192.168.1.4/32     *[BGP/170] 03:16:18, localpref 100
                      AS path: 65001 65004 I, validation-state: unverified
                    >  to 100.1.1.1 via ge-0/0/9.0
                    [BGP/170] 03:14:16, localpref 100
                      AS path: 65002 65004 I, validation-state: unverified
                    >  to 100.1.2.1 via ge-0/0/8.0
192.168.1.5/32     *[BGP/170] 00:57:58, localpref 100, from 192.168.255.3
                      AS path: 65005 I, validation-state: unverified
                    >  to 100.0.1.0 via ge-0/0/1.0, Push 300000, Push 299776(top)
192.168.1.6/32     *[BGP/170] 01:04:54, localpref 100, from 192.168.255.3
                      AS path: 65006 I, validation-state: unverified
                    >  to 100.0.1.0 via ge-0/0/1.0, Push 299984, Push 299776(top)
192.168.1.7/32     *[BGP/170] 01:04:16, localpref 100, from 192.168.255.3
                      AS path: 65006 65007 I, validation-state: unverified
                    >  to 100.0.1.0 via ge-0/0/1.0, Push 299984, Push 299776(top)
192.168.1.8/32     *[BGP/170] 01:04:16, localpref 100, from 192.168.255.3
                      AS path: 65006 65008 I, validation-state: unverified
                    >  to 100.0.1.0 via ge-0/0/1.0, Push 299984, Push 299776(top)

mpls.0: 11 destinations, 11 routes (11 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 3d 20:57:52, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 3d 20:57:52, metric 1
                       to table mpls.0
1                  *[MPLS/0] 3d 20:57:52, metric 1
                       Receive
2                  *[MPLS/0] 3d 20:57:52, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 3d 20:57:52, metric 1
                       to table mpls.0
13                 *[MPLS/0] 3d 20:57:52, metric 1
                       Receive
299808             *[LDP/9] 3d 10:40:56, metric 1
                    >  to 100.0.1.0 via ge-0/0/1.0, Pop
299808(S=0)        *[LDP/9] 3d 10:40:56, metric 1
                    >  to 100.0.1.0 via ge-0/0/1.0, Pop
299824             *[LDP/9] 3d 10:40:56, metric 1
                    >  to 100.0.1.0 via ge-0/0/1.0, Swap 299776
299856             *[VPN/170] 3d 08:43:06
                    >  to 100.1.1.1 via ge-0/0/9.0, Pop
299888             *[VPN/170] 2d 09:07:15
                    >  to 100.1.2.1 via ge-0/0/8.0, Pop

bgp.l3vpn.0: 4 destinations, 4 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.255.3:8:192.168.1.5/32
                   *[BGP/170] 00:57:58, localpref 100, from 192.168.255.3
                      AS path: 65005 I, validation-state: unverified
                    >  to 100.0.1.0 via ge-0/0/1.0, Push 300000, Push 299776(top)
192.168.255.3:8:192.168.1.6/32
                   *[BGP/170] 01:04:54, localpref 100, from 192.168.255.3
                      AS path: 65006 I, validation-state: unverified
                    >  to 100.0.1.0 via ge-0/0/1.0, Push 299984, Push 299776(top)
192.168.255.3:8:192.168.1.7/32
                   *[BGP/170] 01:04:16, localpref 100, from 192.168.255.3
                      AS path: 65006 65007 I, validation-state: unverified
                    >  to 100.0.1.0 via ge-0/0/1.0, Push 299984, Push 299776(top)
192.168.255.3:8:192.168.1.8/32
                   *[BGP/170] 01:04:16, localpref 100, from 192.168.255.3
                      AS path: 65006 65008 I, validation-state: unverified
                    >  to 100.0.1.0 via ge-0/0/1.0, Push 299984, Push 299776(top)

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe01:0/128
                   *[Local/0] 3d 21:13:48
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 3d 21:13:59
                       MultiRecv
```

### PE2
```
root@PE2> show route

inet.0: 8 destinations, 8 routes (8 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

100.0.1.0/31       *[OSPF/10] 3d 20:52:09, metric 200
                    >  to 100.0.2.0 via ge-0/0/1.0
100.0.2.0/31       *[Direct/0] 3d 21:00:50
                    >  via ge-0/0/1.0
100.0.2.1/32       *[Local/0] 3d 21:00:50
                       Local via ge-0/0/1.0
192.168.255.1/32   *[OSPF/10] 3d 10:41:17, metric 200
                    >  to 100.0.2.0 via ge-0/0/1.0
192.168.255.2/32   *[OSPF/10] 3d 20:52:09, metric 100
                    >  to 100.0.2.0 via ge-0/0/1.0
192.168.255.3/32   *[Direct/0] 3d 21:00:50
                    >  via lo0.0
224.0.0.2/32       *[LDP/9] 3d 20:57:47, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 3d 20:56:41, metric 1
                       MultiRecv

inet.3: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.255.1/32   *[LDP/9] 3d 10:41:16, metric 1
                    >  to 100.0.2.0 via ge-0/0/1.0, Push 299808
192.168.255.2/32   *[LDP/9] 3d 20:52:09, metric 1
                    >  to 100.0.2.0 via ge-0/0/1.0

DC-LLC_VRF.inet.0: 12 destinations, 16 routes (12 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

100.2.1.0/31       *[Direct/0] 00:58:36
                    >  via ge-0/0/9.0
100.2.1.0/32       *[Local/0] 00:58:36
                       Local via ge-0/0/9.0
100.2.2.0/31       *[Direct/0] 01:05:18
                    >  via ge-0/0/8.0
100.2.2.0/32       *[Local/0] 01:05:18
                       Local via ge-0/0/8.0
192.168.1.1/32     *[BGP/170] 2d 11:23:51, localpref 100, from 192.168.255.1
                      AS path: 65001 I, validation-state: unverified
                    >  to 100.0.2.0 via ge-0/0/1.0, Push 299856, Push 299808(top)
192.168.1.2/32     *[BGP/170] 2d 09:07:34, localpref 100, from 192.168.255.1
                      AS path: 65002 I, validation-state: unverified
                    >  to 100.0.2.0 via ge-0/0/1.0, Push 299888, Push 299808(top)
192.168.1.3/32     *[BGP/170] 03:16:38, localpref 100, from 192.168.255.1
                      AS path: 65001 65003 I, validation-state: unverified
                    >  to 100.0.2.0 via ge-0/0/1.0, Push 299856, Push 299808(top)
192.168.1.4/32     *[BGP/170] 03:16:38, localpref 100, from 192.168.255.1
                      AS path: 65001 65004 I, validation-state: unverified
                    >  to 100.0.2.0 via ge-0/0/1.0, Push 299856, Push 299808(top)
192.168.1.5/32     *[BGP/170] 00:58:20, localpref 100
                      AS path: 65005 I, validation-state: unverified
                    >  to 100.2.1.1 via ge-0/0/9.0
                    [BGP/170] 01:05:16, localpref 100
                      AS path: 65006 65007 65005 I, validation-state: unverified
                    >  to 100.2.2.1 via ge-0/0/8.0
192.168.1.6/32     *[BGP/170] 01:05:16, localpref 100
                      AS path: 65006 I, validation-state: unverified
                    >  to 100.2.2.1 via ge-0/0/8.0
                    [BGP/170] 00:58:20, localpref 100
                      AS path: 65005 65008 65006 I, validation-state: unverified
                    >  to 100.2.1.1 via ge-0/0/9.0
192.168.1.7/32     *[BGP/170] 01:05:16, localpref 100
                      AS path: 65006 65007 I, validation-state: unverified
                    >  to 100.2.2.1 via ge-0/0/8.0
                    [BGP/170] 00:58:20, localpref 100
                      AS path: 65005 65007 I, validation-state: unverified
                    >  to 100.2.1.1 via ge-0/0/9.0
192.168.1.8/32     *[BGP/170] 01:05:16, localpref 100
                      AS path: 65006 65008 I, validation-state: unverified
                    >  to 100.2.2.1 via ge-0/0/8.0
                    [BGP/170] 00:58:20, localpref 100
                      AS path: 65005 65008 I, validation-state: unverified
                    >  to 100.2.1.1 via ge-0/0/9.0

mpls.0: 11 destinations, 11 routes (11 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 3d 20:57:47, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 3d 20:57:47, metric 1
                       to table mpls.0
1                  *[MPLS/0] 3d 20:57:47, metric 1
                       Receive
2                  *[MPLS/0] 3d 20:57:47, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 3d 20:57:47, metric 1
                       to table mpls.0
13                 *[MPLS/0] 3d 20:57:47, metric 1
                       Receive
299776             *[LDP/9] 3d 20:52:09, metric 1
                    >  to 100.0.2.0 via ge-0/0/1.0, Pop
299776(S=0)        *[LDP/9] 3d 20:52:09, metric 1
                    >  to 100.0.2.0 via ge-0/0/1.0, Pop
299808             *[LDP/9] 3d 10:41:16, metric 1
                    >  to 100.0.2.0 via ge-0/0/1.0, Swap 299808
299984             *[VPN/170] 01:05:16
                    >  to 100.2.2.1 via ge-0/0/8.0, Pop
300000             *[VPN/170] 00:58:20
                    >  to 100.2.1.1 via ge-0/0/9.0, Pop

bgp.l3vpn.0: 4 destinations, 4 routes (4 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.255.1:8:192.168.1.1/32
                   *[BGP/170] 2d 11:23:51, localpref 100, from 192.168.255.1
                      AS path: 65001 I, validation-state: unverified
                    >  to 100.0.2.0 via ge-0/0/1.0, Push 299856, Push 299808(top)
192.168.255.1:8:192.168.1.2/32
                   *[BGP/170] 2d 09:07:34, localpref 100, from 192.168.255.1
                      AS path: 65002 I, validation-state: unverified
                    >  to 100.0.2.0 via ge-0/0/1.0, Push 299888, Push 299808(top)
192.168.255.1:8:192.168.1.3/32
                   *[BGP/170] 03:16:38, localpref 100, from 192.168.255.1
                      AS path: 65001 65003 I, validation-state: unverified
                    >  to 100.0.2.0 via ge-0/0/1.0, Push 299856, Push 299808(top)
192.168.255.1:8:192.168.1.4/32
                   *[BGP/170] 03:16:38, localpref 100, from 192.168.255.1
                      AS path: 65001 65004 I, validation-state: unverified
                    >  to 100.0.2.0 via ge-0/0/1.0, Push 299856, Push 299808(top)

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe03:0/128
                   *[Local/0] 3d 21:14:04
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 3d 21:14:15
                       MultiRecv
```


### P1
```
root@P1> show route

inet.0: 9 destinations, 9 routes (9 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

100.0.1.0/31       *[Direct/0] 3d 20:52:34
                    >  via ge-0/0/0.0
100.0.1.0/32       *[Local/0] 3d 20:52:34
                       Local via ge-0/0/0.0
100.0.2.0/31       *[Direct/0] 3d 20:52:34
                    >  via ge-0/0/1.0
100.0.2.0/32       *[Local/0] 3d 20:52:34
                       Local via ge-0/0/1.0
192.168.255.1/32   *[OSPF/10] 3d 10:41:35, metric 100
                    >  to 100.0.1.1 via ge-0/0/0.0
192.168.255.2/32   *[Direct/0] 3d 20:59:16
                    >  via lo0.0
192.168.255.3/32   *[OSPF/10] 3d 20:52:29, metric 100
                    >  to 100.0.2.1 via ge-0/0/1.0
224.0.0.2/32       *[LDP/9] 3d 20:57:38, metric 1
                       MultiRecv
224.0.0.5/32       *[OSPF/10] 3d 20:56:41, metric 1
                       MultiRecv

inet.3: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

192.168.255.1/32   *[LDP/9] 3d 10:41:35, metric 1
                    >  to 100.0.1.1 via ge-0/0/0.0
192.168.255.3/32   *[LDP/9] 3d 20:52:27, metric 1
                    >  to 100.0.2.1 via ge-0/0/1.0

mpls.0: 10 destinations, 10 routes (10 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

0                  *[MPLS/0] 3d 20:57:38, metric 1
                       to table inet.0
0(S=0)             *[MPLS/0] 3d 20:57:38, metric 1
                       to table mpls.0
1                  *[MPLS/0] 3d 20:57:38, metric 1
                       Receive
2                  *[MPLS/0] 3d 20:57:38, metric 1
                       to table inet6.0
2(S=0)             *[MPLS/0] 3d 20:57:38, metric 1
                       to table mpls.0
13                 *[MPLS/0] 3d 20:57:38, metric 1
                       Receive
299776             *[LDP/9] 3d 20:52:27, metric 1
                    >  to 100.0.2.1 via ge-0/0/1.0, Pop
299776(S=0)        *[LDP/9] 3d 20:52:27, metric 1
                    >  to 100.0.2.1 via ge-0/0/1.0, Pop
299808             *[LDP/9] 3d 10:41:35, metric 1
                    >  to 100.0.1.1 via ge-0/0/0.0, Pop
299808(S=0)        *[LDP/9] 3d 10:41:35, metric 1
                    >  to 100.0.1.1 via ge-0/0/0.0, Pop

inet6.0: 2 destinations, 2 routes (2 active, 0 holddown, 0 hidden)
+ = Active Route, - = Last Active, * = Both

fe80::5200:ff:fe02:0/128
                   *[Local/0] 3d 21:14:19
                       Local via fxp0.0
ff02::2/128        *[INET6/0] 3d 21:14:30
                       MultiRecv
```
