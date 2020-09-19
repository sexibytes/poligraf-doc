---
title: vCenter Credstore
---

Out of the box, **PoliGraf** will not pull any data as it don’t know where your vCenter servers are. First of all, after you’ve deployed it on your platform, you will have to add vCenter information to let the appliance start fetching data. This operation can be achieve from the **Credential Store** tool. Just go on the **PoliGraf Web Admin** dashboard and select **Credential Store**. You will then see the list of all vCenter you already have set up. If you want to add another entry, you just have to type the 3 mandatory parameters and press **Add** and set it up:

- **vCenter IP or FQDN**. In case of FQDN, the appliance must be able to resolve it!
- Username that PoliGraf will use to query the vCenter (any read-only account is enough, you can use SAM, UPN or single user format)
- Password that comes with this username

As we distinguish VI stats from VSAN ones (because **VI stats are pulled every 5 min and VSAN stats every 1 min**), you can choose if you want to query VI, or VSAN, or both by enable/disable it thanks to the **Action** menu on the right of the vCenter.

*Note: The credentials are used to create a session that will last as long as possible using a session file to avoid login/logoff events.*

{{< hint info >}}
As soon as you added vCenter information, offline inventory will be generated. Just grab a coffee and wait a few minutes for PoliGraf to retrieve stats, and start Monitoring, like a boss!
{{< /hint >}}

![PoliGraf Menu](/media/vcenter-credstore.png)
