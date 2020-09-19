---
title: vSAN Capacity
---


![VMware_VSAN_Capacity](/media/vmware_vsan_capacity_s.png)

As per [VMware Virtual SAN 6.0 Design and Sizing Guide](http://www.vmware.com/files/pdf/products/vsan/VSAN_Design_and_Sizing_Guide.pdf): “VMware is recommending, if possible, **30% free capacity across the Virtual SAN datastore**. The reasoning for this slack space size is that **Virtual SAN begins automatic rebalancing when a disk reaches the 80% full threshold**, generating rebuild traffic on the cluster”. Moreover, if one disk (or flash capacity) of a disk group is full, the VM with objects on it are stunned until vSAN has finish the rebalance of the objects.

In vSAN Observer, you can check the upper, lower and average disk (or flash capacity) usage per host but not per cluster and most importantly you won’t be able to see the trend so **you won’t be able to predict anything**.

![Capacity](/media/2015-09-26_17-31-44.png)

The **vSAN Capacity dashboard** shows you the nodes capacity metrics of the entire cluster and allow you to **anticipate futur storage needs**. For each host, the shadow represents the min/max area of the diskgroups and the dark line represents the average.
