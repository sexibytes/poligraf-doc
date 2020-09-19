---
title: Multi Cluster Top N VM Snapshot
---


In the history of VMware monitoring tools, PoliGraf 0.99d is the first to introduce VM snapshots monitoring:

![](/media/vmware_multi_cluster_top_n_vm_snapshot.jpg)

Now you can analyze what’s happening during your backup window and monitor with a surgical precision, per cluster, **the snapshot size evolution of your VMs**. With this new dashboard, you won’t miss ANY forgotten snaps EVER!

![](/media/vmware_multi_cluster_top_n_vm_snaphot_xl.png)

And since we leverage the [parent](http://pubs.vmware.com/vsphere-6-5/index.jsp?topic=%2Fcom.vmware.wssdk.apiref.doc%2Fvim.vm.device.VirtualDisk.SparseVer2BackingInfo.html) property of the vdisk objects to determine if it’s a real snapshot (or a vdisk with a funny name), you can also keep track of [**the hidden snapshots**](https://kb.vmware.com/kb/1002310) (aka non-consolidated) with this dashboard.
