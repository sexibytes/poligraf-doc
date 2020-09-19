As **PoliGraf** will retrieve information on vCenter servers, it’s important to keep track of the time it takes to query API. So we added a **Pull Exec Time** dashboard that will keep track of these query durations for all calls that are made by the appliance (VI, VSAN and inventory). Usually, scripts run in a few seconds, so if queries took too long, you’ll be able to see it right away:

![PoliGraf_Pull_Exec_Time_2](/media/poligraf_pull_exec_time_2.png)
