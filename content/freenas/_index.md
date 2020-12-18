---
title: FreeNAS
weight: 30
---


Starting [from version 9.10](http://download.freenas.org/9.10/RELEASE/ChangeLog), FreeNAS allows users to set a “[Remote Graphite Server](https://doc.freenas.org/9.10/freenas_system.html#advanced)” target to send all the metrics harvested by Collectd. Guess what would make a nice Graphite target!

![FreeNAS](/media/freenas.png)

The **FreeNAS** SexiPanel (_Available in PoliGraf 0.99c_) let you monitor (one of) your FreeNAS server(s) in a “single pane of glass” experience.

The “**partition**” and “**interface**” drop down menus let you select one, some or all of the **ZFS datasets** and network interfaces, including LACP LAGG. The ARC row let you check the **ZFS Adaptive Replacement Cache** usage and hit ratio. The HD row is a stacked histogram of the disks IOs.

Say goodbye to the oldish RRD style reporting tabs, just set the ip address of your PoliGraf appliance as Graphite target and reboot your FreeNAS to apply 😉

![FreeNAS](/media/freenas_reporting.png)
