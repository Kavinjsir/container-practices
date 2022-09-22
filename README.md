### A Demo of Nginx with SSL for Subdomains

#### Quick Start

**1. Modify you local dns**

Add following 2 lines in your host config(usually `/etc/hosts`):

```
127.0.0.1 a.example.com
127.0.0.1 b.example.com
```

**2. Launch the containers of apps & nginx**

```shell
./run.sh
```

**3. Verify the accessibility through `curl`**

```shell
# Request "a.example.com" should receive greeting from App 1
❯ curl --insecure https://a.example.com
Greeting from App 1

# Request "b.example.com" should receive greeting from App 2
❯ curl --insecure https://b.example.com
Greeting from App 2!
```
