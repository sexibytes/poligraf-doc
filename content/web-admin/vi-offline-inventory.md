---
title: VI Offline Inventory
---

When you work with several vCenter on your platform, it could be ~~a pain in the ...~~ tricky to find virtual machine for daily-basis administration tasks. What we used to do during our past job experience is to build some static inventory, to be able to search quickly cross-vCenter some virtual machine information. It can be really useful, specially if you have an outage and you want to see on which ESX was your vCenter VM.

So we thought about adding this "feature" to **PoliGraf** as it could be useful to another admin. You could find this offline inventory available on the **PoliGraf VI Offline Inventory** dashboard. It’s generated every 1 hour _(since 0.99e, previously it was 6 hours)_ and let you search in any column listed. As we added a lot of info, we wanted to not make too messy, so we hid by default some columns. On the top of the page, you will be able to click on each button that represent a column to dynamically show/hide it.

![offline-inventory](/media/offline-inventory.gif)

Starting from PoliGraf 0.99d, you can click on any VM or Cluster to be redirected on a the corresponding [VM Stats](http://www.PoliGraf.fr/vsphere-sexipanels/#vsphere-top-n-vm-stats) or [Cluster FullStats](http://www.PoliGraf.fr/vsphere-sexipanels/#cluster-fullstats) dashboard. We’ve also added **“blue folder” path** property:

![](/media/poligraf_vi_offline_inventory.png)