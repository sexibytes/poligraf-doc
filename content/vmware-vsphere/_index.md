---
title: VMware vSphere
weight: 20
---


**Fast**. Very fast. That’s what we had in mind when we designed PoliGraf. When you need vSphere metrics, the obvious way is the [PerformanceManager](http://pubs.vmware.com/vsphere-60/topic/com.vmware.wssdk.apiref.doc/vim.PerformanceManager.html), but we need something faster so we choosed managed object properties and quickstats like [ResourcePoolQuickStats](http://pubs.vmware.com/vsphere-60/topic/com.vmware.wssdk.apiref.doc/vim.ResourcePool.Summary.QuickStats.html). If we have no other choice, we failback to the PerformanceManager but we only query the last 15 samples of the RealTime [samplingPeriod](http://pubs.vmware.com/vsphere-60/topic/com.vmware.wssdk.apiref.doc/vim.HistoricalInterval.html#samplingPeriod) since **we pull vSphere metrics every 5 minutes**.
