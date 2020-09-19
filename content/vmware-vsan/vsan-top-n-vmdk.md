---
title: Top N vmdk
---


![VSAN_Top_N_vmdk_avg](/media/vsan_top_n_vmdk_avg.gif)

The **vSAN Top N vmdk** dashboard (added in PoliGraf 0.99a) let you immediately identify the most active VMs on your vsanDatastore “like” the infamously slow **Virtual Machine Disk (Top 10)** which is not available for vSAN datastores :

![legacy_top_n](/media/legacy_top_n.gif)

You’ll be able to observe flat vmdk as well as **snapshots redo logs** activity, select only few vm disks to inspect and also chose between **Current**, **Average** or **Max** consolidation over the selected time range:

![VSAN_Top_N_vmdk_avg_N10](/media/vsan_top_n_vmdk_avg_n10.gif)

![VSAN_Top_N_vmdk_avg_N3](/media/vsan_top_n_vmdk_avg_n3.gif)
