In 0.99e version, we’ve added the **Export / Import** section to let you migrate your PoliGraf configuration (vCenter credentials) AND data (wisper files) from one appliance to another.

![](/media/export-import.png)

The process is fairly simple, you click on **Generate export bundle** and the appliance creates you an iso file to download (this might take from few seconds to few minutes depending on your environment size). If a dump is already present, **Generate export bundle** function will overwrite it without prompt.

![](/media/export-iso.png)

Once you got the iso file, you map it to your new PoliGraf VM’s CD-ROM drive, refresh the page and then click on **Run import process** (This might also take a while depending on your environment). At the end of the process, the iso is ejected for safety purpose:

![](/media/sexigraf_export_import_099f_0.png)

{{< hint info >}}
The import only applies to vCenter connections and collected metrics, **NO PASSWORD** will be changed in the process.
{{< /hint >}}

{{< hint warning >}}
Be aware that importing a dump from or to a different version is **not supported** even if it is supposed to work.
{{< /hint >}}

{{< hint danger >}}
Also, be very careful when importing since the process will overwrite anything in its way so it might be a good thing in a migration scenario but also a disaster if you do it on the wrong appliance. Anyway, **we always advise you to make a backup or create a snapshot before patching or importing data on your VMs**.
{{< /hint >}}

The export **won’t** contain any of your **custom Grafana dashboards** and you’ll need to export/import via json files yourself [as documented on the Grafana’s website](http://docs.grafana.org/reference/export_import/).
