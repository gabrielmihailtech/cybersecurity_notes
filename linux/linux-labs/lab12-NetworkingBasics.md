# Lab 12 - Networking Basics

Commands:

- ip addr
- ip link
- ss -tuln
- ss -tulpn
- ping
- ip route

Learned:

- Linux network information can be viewed using ip commands
- loopback interface is represented by lo
- eth0 is the primary network interface
- ss displays listening ports and network connections
- ping tests network connectivity
- ip route displays routing information

Examples:

Display IP addresses:

```bash
ip addr
```

Observed:

```text
172.20.39.214
127.0.0.1
```

Display interfaces:

```bash
ip link
```

Observed:

```text
lo
eth0
```

Display listening services:

```bash
ss -tuln
```

Display listening services and associated processes:

```bash
sudo ss -tulpn
```

Test local connectivity:

```bash
ping 127.0.0.1
```

Result:

```text
0% packet loss
```

Test external connectivity:

```bash
ping 8.8.8.8
```

Result:

```text
0% packet loss
```

Display routing table:

```bash
ip route
```

Observed:

```text
default via 172.20.32.1 dev eth0
```

Observed IP Address:

```text
172.20.39.214
```

Observed Gateway:

```text
172.20.32.1
```

Important Concepts:

Localhost:

```text
127.0.0.1
```

Loopback Interface:

```text
lo
```

Primary Interface:

```text
eth0
```

Gateway:

```text
172.20.32.1
```

Key Takeaways:

- ip addr displays IP addresses
- ip link displays interfaces
- ss shows listening ports and connections
- ping verifies connectivity
- ip route identifies the default gateway
- Network visibility is essential for troubleshooting and SOC investigations
