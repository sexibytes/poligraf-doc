---
title: Multi Cluster Top N VM Overcommit
---


We could have added those graphs in the **Top N VM Stats** dashboard but we wanted to kept the bad and the ugly apart from the good. Since PoliGraf 0.99b you can also monitor the top N overcommited**\*** VM (1 to 20 VM per graph).

[![](/media/vmware_multi_cluster_top_n_vm_overcommit.png)](http://www.poligraf.io/vsphere-sexipanels/vmware_multi_cluster_top_n_vm_overcommit/)

This dashboard will help you to identify situations like **memory limits**, vm that have been in contention in the past with remaining **zipped/swapped** pages or **[idle tax](http://www.yellow-bricks.com/2010/03/11/mem-idletax/)**.

**\*** The graph names match the [**Counters** names of the **Performance Manager**](http://pubs.vmware.com/vsphere-60/index.jsp?topic=%2Fcom.vmware.wssdk.apiref.doc%2Fvim.PerformanceManager.html) to let you dig into the details if you want to.
