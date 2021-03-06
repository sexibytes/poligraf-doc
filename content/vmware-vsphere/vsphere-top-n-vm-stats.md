---
title: All Cluster Top N VM Stats
---


Starting from PoliGraf 0.99b you can monitor the top N VM quickstats**\*** (1 to 20 VM per graph). Now you can find the bad \*sses of your datacenters!

[![](/media/vmware_multi_cluster_top_n_vm_stats.png)](http://www.poligraf.io/vsphere-sexipanels/vmware_multi_cluster_top_n_vm_stats/)

Of course you can also search and pick some VM of your choice to compare their stats. The legend is formated as such to help you locate any tango: **clustername.vmname**

[![](/media/vmware_multi_cluster_top_n_vm_stats_Select.png)](http://www.poligraf.io/vsphere-sexipanels/vmware_multi_cluster_top_n_vm_stats_select/)

In the PoliGraf 0.99d release, we revisited this dashboard to add **snapshot usage** (storage.delta), **CPU & MEM usage in %**, the world famous **CPU Ready** metric ([aka %RDY](https://communities.vmware.com/docs/DOC-9279)), **CPU Latency** ([aka %lat\_c](http://virtual-hike.com/high-lat_c-values-in-esxtop/)) and **maxTotalLatency**. Now you can check everything about all or some specific VMs in a single pane of glass:

[![](/media/vmware_all_cluster_top_n_vm_stats.png)](http://www.poligraf.io/vsphere-sexipanels/vmware_all_cluster_top_n_vm_stats/)

In 0.99e version, we’ve added vm network and disk usage:

[![](/media/vmware_multi_cluster_top_n_vm_stats_hdd.jpg)](http://www.poligraf.io/vsphere-sexipanels/vmware_multi_cluster_top_n_vm_stats_hdd/)

[![](/media/vmware_multi_cluster_top_n_vm_stats_net.jpg)](http://www.poligraf.io/vsphere-sexipanels/vmware_multi_cluster_top_n_vm_stats_net/)

You may want a **top 5 VM per cluster** instead? We did that too 😉

Check out the **Multi Cluster Top N VM QuickStats dashboard** and simply slide over to reveal the usual suspects:

[![](/media/Vmware_multi_cluster_top_n_vm_quickstats.png)](http://www.poligraf.io/vsphere-sexipanels/vmware_multi_cluster_top_n_vm_quickstats/)

[![](/media/vmware_multi_cluster_top_n_vm_quickstats_zoom.png)](http://www.poligraf.io/vsphere-sexipanels/vmware_multi_cluster_top_n_vm_quickstats_zoom/)

In PoliGraf 0.99f, we've added a variant of that dashboard with **overcommit metrics** but without the **Top N** feature for those with big inventory just wanting to compare a bunch of VMs: **VMware All Cluster VM Stats**

[![](/media/vmware_all_cluster_vm_stats.png)](http://www.poligraf.io/vmware_all_cluster_vm_stats/)

In version 0.99g we've added CPU Wait metric from which we deduced CPU idle metric in order to only keep the I/O wait : "[The wait total includes time spent the CPU Idle, CPU Swap Wait, and CPU I/O Wait states](https://vdc-download.vmware.com/vmwb-repository/dcr-public/b50dcbbf-051d-4204-a3e7-e1b618c1e384/538cf2ec-b34f-4bae-a332-3820ef9e7773/cpu_counters.html)."

![](/media/099g_cpu_wait.png)