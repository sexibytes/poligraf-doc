---
title: Windows
weight: 40
---

Leveraging the [built-in Graphite listener](http://www.PoliGraf.fr/features/) of PoliGraf, we introduced Windows support in version 0.99c with basic cpu-ram-hdd metrics :

![Windows_SSC](/media/windows_ssc.png)

To push the metrics we chose to use [the recommended Windows version of collectd](https://collectd.org/features.shtml), SSC Serv.

![SSC_Graphite](/media/ssc_graphite.png)

After instaling the lightweight agent, just add your PoliGraf appliance IP address with “SSC.” as prefix and you’re good to go.

![SSC_Graphite_server](/media/ssc_graphite_server.png)

Now you can monitor your **VEEAM** proxies, like a boss!
