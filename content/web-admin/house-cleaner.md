The House Cleaner (formerly Stats Remover) will let you manage Graphite data (Whisper files) and vCenter session data (Token files). Through this web-ui, you will be able to remove legacy or orphaned stats (i.e. after datastore removal), vCenter session files (for authentication troubleshooting) and oldest Whisper files that may no longer be used. They will be displayed in a nice data tree and will let you select any (one or more) files in order to remove them (don’t be afraid, it will ask you some noisy confirmation before hurting your **PoliGraf**). As Grafana is based on dynamic query on whisper files, the effect will be immediate, you will not need to restart anything, what you wanted gone is gone for sure!

![](/media/house-cleaner-01.gif)

![](/media/house-cleaner-02.gif)

In PoliGraf 0.99d we limit the scope to folders to avoid timeouts in big environments. We also added the “Auto Purge” feature (disabled by default) so **you don’t have to worry about removed objects anymore** like deleted items, temporary datastores, VM migrated from a cluster to another one, etc… We hard coded this feature to 120 days but we plan to make this setting tunable:

![](/media/house-cleaner-03.png)
