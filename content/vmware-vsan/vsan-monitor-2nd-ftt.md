---
title: vSAN Monitor 2nd FTT
---


As described in [VMware vSAN 6.6 Technical Overview white paper](https://storagehub.vmware.com/export_to_pdf/vmware-vsan-6-6-technical-overview-1), vSAN 6.6 introduce secondary level of failures to tolerate ([SFTT](http://cormachogan.com/2017/04/11/whats-new-vsan-6-6/)) for stretched clusters:

> Starting with vSAN 6.6, it is possible to configure a secondary level of failures to tolerate. This feature enables resiliency within a site, as well as, across sites. For example, RAID-5 erasure coding protects objects within the same site while RAID-1 mirroring protects these same objects across sites.

![](/media/vsan_sftt.png)

After snooping into the **undocumented** metrics, we discovered that the SFTT traffic is “monitorable” through 2 new counters called “**proxy**” and “**anchor**” so, starting from v0.99d, we added a dedicated dashboard inspired from the vSAN Monitor one. Meet **vSAN Monitor 2nd FTT**:

[![](/media/vmware_vsan_monitor_2nd_ftt.png)](http://www.poligraf.fr/vsan-sexipanels/vmware_vsan_monitor_2nd_ftt/)

![](/media/vmware_vsan_monitor_2nd_ftt_anchor_proxy.jpg)

Since we had some free space left on the dashboard, we also added some [UNMAP](https://kb.vmware.com/kb/2014849) metrics.