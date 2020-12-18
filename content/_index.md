---
title: Documentation
---

<!-- markdownlint-capture -->
<!-- markdownlint-disable MD033 -->

<span class="badge-placeholder">[![GitHub release](https://img.shields.io/github/v/release/sexibytes/poligraf-doc)](https://github.com/sexibytes/poligraf-doc/releases/latest)</span>
<span class="badge-placeholder">[![GitHub contributors](https://img.shields.io/github/contributors/sexibytes/poligraf-doc)](https://github.com/sexibytes/poligraf-doc/graphs/contributors)</span>
<span class="badge-placeholder">[![License: MIT](https://img.shields.io/github/license/xoxys/hugo-geekdoc)](https://github.com/xoxys/hugo-geekdoc/blob/master/LICENSE)</span>

<!-- markdownlint-restore -->

Here is the official documentation for our PoliGraf project.
You'll find on the left menu all the documentation pages, grouped by category

## Web Admin

What we wanted to achieve was to make an appliance as easy to use as possible. Therefore we developed some tools to make your life easier using PoliGraf. First, the Home page let you monitor the health of your appliance thanks to collectd. Every tools are available through the web interface thanks to predefined dashboards like PoliGraf Web Admin or PoliGraf VI Offline Inventory. Just navigate to your PoliGraf web-ui with your favorite browser and select one of these dashboards. You will have access then to the tool grid which let you select what you want to access to. As we will add more features to PoliGraf, we may also add other web tools in this section, so it may evolve in the future.

## VMware VSAN

The metrics used in the various vSAN dashboards are collected **every minutes** using to the [QueryVsanStatistics API method of HostVsanInternalSystem](http://pubs.vmware.com/vsphere-60/index.jsp?topic=%2Fcom.vmware.wssdk.apiref.doc%2Fvim.host.VsanInternalSystem.html). With some json ticks, it is possible to access any metrics from the vSAN cluster. And guess what! We’re already working on other cool SexiPanels for VSAN...

## VMware vSphere

**Fast**. Very fast. That’s what we had in mind when we designed PoliGraf. When you need vSphere metrics, the obvious way is the [PerformanceManager](http://pubs.vmware.com/vsphere-60/topic/com.vmware.wssdk.apiref.doc/vim.PerformanceManager.html), but we need something faster so we choosed managed object properties and quickstats like [ResourcePoolQuickStats](http://pubs.vmware.com/vsphere-60/topic/com.vmware.wssdk.apiref.doc/vim.ResourcePool.Summary.QuickStats.html). If we have no other choice, we failback to the PerformanceManager but we only query the last 15 samples of the RealTime [samplingPeriod](http://pubs.vmware.com/vsphere-60/topic/com.vmware.wssdk.apiref.doc/vim.HistoricalInterval.html#samplingPeriod) since **we pull vSphere metrics every 5 minutes**.

## FreeNAS

Starting [from version 9.10](http://download.freenas.org/9.10/RELEASE/ChangeLog), FreeNAS allows users to set a “[Remote Graphite Server](https://doc.freenas.org/9.10/freenas_system.html#advanced)” target to send all the metrics harvested by Collectd. Guess what would make a nice Graphite target! The **FreeNAS** SexiPanel (_Available in PoliGraf 0.99c_) let you monitor (one of) your FreeNAS server(s) in a “single pane of glass” experience. The “**partition**” and “**interface**” drop down menus let you select one, some or all of the **ZFS datasets** and network interfaces, including LACP LAGG. The ARC row let you check the **ZFS Adaptive Replacement Cache** usage and hit ratio. The HD row is a stacked histogram of the disks IOs. Say goodbye to the oldish RRD style reporting tabs, just set the ip address of your PoliGraf appliance as Graphite target and reboot your FreeNAS to apply 😉

## Windows

Leveraging the [built-in Graphite listener](http://www.PoliGraf.fr/features/) of PoliGraf, we introduced Windows support in version 0.99c with basic cpu-ram-hdd metrics. To push the metrics we chose to use [the recommended Windows version of collectd](https://collectd.org/features.shtml), SSC Serv. After instaling the lightweight agent, just add your PoliGraf appliance IP address with “SSC.” as prefix and you’re good to go. Now you can monitor your **VEEAM** proxies, like a boss!

## S.M.A.R.T.

Since the first release we wanted to add a **SMART** counters dashboard because we were so inspired by the [Backblaze reports](https://www.backblaze.com/blog/what-smart-stats-indicate-hard-drive-failures/). But we never found a proper way to get those stats from any kind of NAS so we decided to rely on a custom script that pushes the data to graphite using netcat 😉

## pfSense

Because we love and use pfSense very much since the **m0n0wall** fork, we decided to make a great dashboard with system metrics, interface statistics but most importantly [the **pfinfo** data which let you **monitor the packet filtering**](https://docs.netgate.com/pfsense/en/latest/monitoring/status/pfinfo.html) service of the firewall.
