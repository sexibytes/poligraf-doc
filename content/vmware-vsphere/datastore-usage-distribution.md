Ever Wonder what your datastores are full of? How much swap and snapshots are consuming per cluster?

![](/media/vmware_datastore_usage_distribution_legacy.png)

Since PoliGraf 0.99d the **Multi Cluster Datastore Usage Distribution** dashboard let you monitor the datastore usage per [filetype](http://pubs.vmware.com/vsphere-6-5/index.jsp?topic=%2Fcom.vmware.wssdk.apiref.doc%2Fvim.vm.FileLayoutEx.FileType.html) like the old-shool VMware pie chart but Harder, Better, Faster, Stronger and at the cluster level:

[![](/media/vmware_multi_cluster_datastore_usage_distribution.png)](http://www.poligraf.io/vsphere-sexipanels/vmware_multi_cluster_datastore_usage_distribution/)

Because the [Disk extent (-flat/-delta/-s/-rdm/-rdmp.vmdk) file](http://pubs.vmware.com/vsphere-6-5/index.jsp?topic=%2Fcom.vmware.wssdk.apiref.doc%2Fvim.vm.FileLayoutEx.FileType.html) VMware File-type was a bit too inclusive, we took the liberty to split it to add new ones like rdmExtent, rdmpExtent, snapshotExtent and snapshotDescriptor. In the future, we also plan to add vsanSparseVariant.

[![](/media/vmware_multi_cluster_datastore_usage_distribution_rdm.png)](http://www.poligraf.io/vsphere-sexipanels/vmware_multi_cluster_datastore_usage_distribution_rdm/)

Since we've added a FileType selector, you can pick snapshot file types and track the waste space on your entire infrastructure! And just because we know you’d love it, we have also added a **snapshot counter on the right Y axis** 😉

[![](/media/vmware_multi_datastore_usage_distribution_snapradar.jpg)](http://www.poligraf.io/vsphere-sexipanels/vmware_multi_datastore_usage_distribution_snapradar/)

Last but not least, if you need to see the big picture, we also created the **All Datastore Usage Distribution** dashboard:

[![](/media/vmware_all_datastore_usage_distribution.png)](http://www.poligraf.io/vsphere-sexipanels/vmware_all_datastore_usage_distribution/)
