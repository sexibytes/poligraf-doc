This dashboard allows you to compare the selected vmnic of the selected ESX in your favorite cluster. If this cluster is contained in a blade enclosure, **you’re now able to check what is going in and out from your chassis**. Noticed the cacti style of the graphs?

[![](/media/vmware_network.png)](http://www.poligraf.io/vsphere-sexipanels/vmware_network/)

In version 0.99e, we’ve added the [droppedTX, droppedRX, errorsTX and errorsRX counters](https://vdc-repo.vmware.com/vmwb-repository/dcr-public/fe08899f-1eec-4d8d-b3bc-a6664c168c2c/7fdf97a1-4c0d-4be0-9d43-2ceebbc174d9/doc/network_counters.html) (on the right Y axis) so can have a bit of history for those metrics in your favourite tool:

![](/media/poligraf_network_errors.png)
