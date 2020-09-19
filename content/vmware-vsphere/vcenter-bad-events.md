---
title: vCenter Bad Events
---


After years of [SexiLog](http://www.sexilog.fr) feedback, we figured out that some VMware users are well aware of the ESXi logs monitoring benefits. We also discovered that the configuration needed to get syslog working is sometime confusing (syslog target, firewall, etc..) but also that the security behind it is also a concern. And of course there is the big players with thousands of ESXi to manage. For all those reasons, starting from PoliGraf 0.99f, we now included event monitoring! Bad ones obviously 😉

[![](/media/poligraf099f_exevents-1.png)](http://www.poligraf.io/poligraf099f_exevents-2/)

You’ll now be able to see what is happening on your infrastructure (at **computeResource level** so even standalone hosts are included) without anything more to do but deploy PoliGraf and enjoy our new dashboard with **events per Cluster** on top and **events per TypeId** at the bottom. Behind the scene, [we fetch the list of “bad” events available on your vCenter](http://www.hypervisor.fr/?p=5229) so even future vSphere version will be supported and then we ask the **eventManager** if those events occurred in the last 5 minutes. Here is a small example of what we could get from our “test” setup:

> BadUsernameSessionEvent  
> ClusterOvercommittedEvent  
> com\_vmware\_vc\_certmgr\_HostCertExpirationImminentEvent  
> com\_vmware\_vc\_HA\_DasHostFailedEvent  
> com\_vmware\_vc\_ha\_VmRestartedByHAEvent  
> com\_vmware\_vc\_VmDiskConsolidationNeeded  
> esx\_audit\_host\_boot  
> esx\_problem\_net\_connectivity\_lost  
> esx\_problem\_net\_vmknic\_ip\_duplicate  
> esx\_problem\_scsi\_device\_state\_permanentloss  
> esx\_problem\_storage\_apd\_start  
> esx\_problem\_storage\_redundancy\_lost  
> esx\_problem\_visorfs\_ramdisk\_inodetable\_full  
> esx\_problem\_vmfs\_heartbeat\_timedout  
> esx\_problem\_vmfs\_nfs\_server\_disconnect  
> esx\_problem\_vmfs\_resource\_corruptondisk  
> esx\_problem\_vsan\_no\_network\_connectivity  
> InsufficientFailoverResourcesEvent  
> msg\_snapshot\_quiesce\_timeout  
> VmInstanceUuidConflictEvent  
> VmMacConflictEvent  
> VmMaxRestartCountReached  
> VmOrphanedEvent  
> vob\_fssvec\_lookup\_file\_failed  
> vob\_vmotion\_transmit\_vbuf\_not\_connected

[![](/media/vcenter_bad_events_snapshot.png)](http://www.poligraf.io/vcenter_bad_events_snapshot/)

[![](/media/vcenter_bad_events_ha.png)](http://www.poligraf.io/vcenter_bad_events_ha/)

[![](/media/vcenter_bad_events_ssl.png)](http://www.poligraf.io/vcenter_bad_events_ssl/)

This is more than enough for most of any VMware admin but remember, if you want more, you need syslog 😉
