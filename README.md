# Cook-SW-Switching

### Let's try MTCP
For MTCP we should first have the DPDK working in our systems, which it does have a very adequet documentation
for this purpose. Actually, they have their own DPDK modified in the repository.

####What config worked for me
For running the sample applications these commands worked for me:
`sudo ./epwget 10.10.1.2/file.txt 1000 -f epwget.conf -N 8 -lc 0xFF`
`sudo ./epserver -p /users/alireza/www -f epserver.conf -N 1 -c 0x1`

#### server arp
```
ARP_ENTRY 1
# 10.10.1.1/24 00:8c:fa:f7:58:38
10.10.1.2/24 00:8c:fa:f7:33:3c
```

#### server route
```
ROUTES 1
10.10.1.0/24 dpdk0
```

#### client arp
```
ARP_ENTRY 1
# 10.10.1.1/24 00:8c:fa:f7:58:38
10.10.1.2/24 00:8c:fa:f7:33:3c
```

#### client route
```
ROUTES 1
10.10.1.0/24 dpdk0
```
