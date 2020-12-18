---
title: pfSense
weight: 60
---

Because we love and use pfSense very much since the **m0n0wall** fork, we decided to make a great dashboard with system metrics, interface statistics but most importantly [the **pfinfo** data which let you **monitor the packet filtering**](https://docs.netgate.com/pfsense/en/latest/monitoring/status/pfinfo.html) service of the firewall.

![](/media/pfsense_0.png)

All you need to do is to install the pfSense **Telegraf** package and configure it EXACTLY as follow:

![](/media/pfsense_telegraf_install.png)

![](/media/pfsense_telegraf_config.png)

```text
[[outputs.graphite]]
servers = ["192.168.0.1:2003"]
prefix = "pfsense"
template = "host.measurement.tags.field"
timeout = 2
```

You can even monitor up to 4 FQDN/IP as a bonus.
