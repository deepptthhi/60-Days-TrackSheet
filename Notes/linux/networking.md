
## What is Networking?

Networking is the process of connecting computers so they can communicate and share data with each other.

In Linux, networking allows you to connect to the internet, communicate with other devices, transfer files, and access remote systems.


## Checking Your IP Address

To view your IP address:

```bash
ip addr
```

Or simply display your system's IP address:

```bash
hostname -I
```

Your IP address is used to identify your computer on a network.



## Testing Internet Connectivity

To check if your system can reach another device or website:

```bash
ping google.com
```

If you receive replies, your internet connection is working.

Stop the command by pressing:

```text
Ctrl + C
```


## Viewing Network Interfaces

To see all network interfaces (like Wi-Fi or Ethernet):

```bash
ip link
```

This shows whether each network interface is active or inactive.


## Viewing Routing Information

To display the routing table:

```bash
ip route
```

The routing table tells Linux where to send network traffic.


## DNS Lookup

DNS (Domain Name System) converts website names into IP addresses.

To look up the IP address of a website:

```bash
nslookup google.com
```

Another commonly used command is:

```bash
dig google.com
```

Both commands help troubleshoot DNS-related issues.

## Viewing Active Network Connections

To display active network connections and listening ports:

```bash
ss
```

This helps you see which applications are using the network.


## Downloading Files

Using `wget`:

```bash
wget https://example.com/file.zip
```

Using `curl`:

```bash
curl https://example.com
```

- `wget` is mainly used for downloading files.
- `curl` is commonly used to send requests to websites and APIs.


## Useful Commands

```bash
ip addr        # Show IP address
hostname -I    # Display IP address
ping           # Test internet connection
ip link        # View network interfaces
ip route       # Show routing table
nslookup       # DNS lookup
dig            # Advanced DNS lookup
ss             # View network connections
wget           # Download files
curl           # Send network requests
```

## Quick Summary

- Networking allows computers to communicate with each other.
- Use `ip addr` or `hostname -I` to check your IP address.
- Use `ping` to test internet connectivity.
- Use `ip link` to view network interfaces.
- Use `ip route` to see the routing table.
- Use `nslookup` or `dig` to perform DNS lookups.
- Use `ss` to check active network connections.
- Use `wget` and `curl` to download data or send requests.


## Commands to Remember

```bash
ip addr
hostname -I
ping google.com
ip link
ip route
nslookup google.com
dig google.com
ss
wget URL
curl URL
```