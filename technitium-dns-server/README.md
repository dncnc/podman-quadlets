# Technitium DNS Server Instructions

## As a Rootful Container

## As a Rootless Container

### Additional Notes
1. A collision with aardvark-dns on port 53 is possible causing the service to fail to start.  To get around this, edit or create /etc/containers.conf with the entry below to instruct podman to use another port for dns such as port 54.  Choose whatever port is suitable for your system.
```
    ...
    [network]
    dns_bind_port = 54
    ...
```
2. Steps to create a user to run the rootless container
