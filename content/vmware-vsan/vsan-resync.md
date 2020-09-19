---
title: Resync
---


![VMware_VSAN_Resync_WebClient](/media/vmware_vsan_resync_webclient.png)

Instead of endlessly clicking on the refresh button in the “Resyncing Components” tab of the WebClient, we added the vSAN Resync dashboard since PoliGraf 0.99b:

![VMware_VSAN_Resync](/media/vmware_vsan_resync.png)

Now you can really **see** what’s going on when objects are being resynced, rebuilded or [rebalanced](http://cormachogan.com/2015/04/22/vsan-6-0-part-9-proactive-re-balance/). We also added a **Recovery Rate** graph to check how fast your vSAN backend performs.

Starting from version 0.99e, we pushed even further and leveraged the vSAN 6.7 API when available. [In vSAN 6.7 VMware introduced the Sync State Reason](https://code.vmware.com/apis/398/vsan#/doc/vim.vsan.host.VsanComponentSyncState.html) so you also know **WHY** the components are being (re)sync. And if some components are synced for several reasons, you’ll know it too of course. Only in PoliGraf 😉

> The list of reasons indicate why the component went into syncing state. The API returns full list of reasons for background. However, sometimes it’s userful to generate an aggregate reason, in which case the following priorities could be used:
> 
> P0: “evacuate” ()  
> P1: “dying\_evacuate” ()  
> P2: “rebalance” ()  
> P3: “repair”, “reconfigure” ()  
> P4: “stale”
> 
> **dying\_evacuate**: The component is being moved out when a disk is going to die.  
> **evacuate**: The component is created and resyncing after evacuate disk group or host to ensure accessibility and full data evacuation.  
> **rebalance**: The component is created and resyncing for rebalancing.  
> **reconfigure**: The component is created and resyncing after vSAN object was resized or its policy was changed.  
> **repair**: The component is created and resyncing to repair a bad component.  
> **stale**: The component is syncing because it was stale.

![](/media/poligraf_resync_67.png)
