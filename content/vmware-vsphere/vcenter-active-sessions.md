---
title: vCenter Active Sessions
---


Sometimes you may need to monitor [vCenter active sessions](https://code.vmware.com/apis/358/vsphere#/doc/vim.SessionManager.html#field_detail) for troubleshooting purpose since, even if [it’s not officially documented](https://www.vcdx200.com/2017/02/maximum-client-sessions-vcenter-server.html) (yet), some of us knows the famous “[SOAP session count limit reached](https://kb.vmware.com/s/article/2004663)” error around 2000 active sessions. In Sexigraf 0.99e update, we’ve added a dashboard to let you visualize the active sessions count for every vCenter registered in the credentials store **with a user granted with “view and stop sessions” role**. Read only accounts won’t work.

[![](/media/vmware_vcenter_active_sessions.png)](http://www.poligraf.io/vsphere-sexipanels/vmware_vcenter_active_sessions/)

But we didn’t stopped there, we also added a count **per username** (the dashed lines). it’s PoliGraf after all 😉

![](/media/vmware_vcenter_active_sessions_ex.png)

The hover tooltip will show you the vCenter total active sessions on top of the list and all the accounts connected. In the screenshot above we can see that the NetBackup account is the reason of the peak. Backup time obviously 🙂
