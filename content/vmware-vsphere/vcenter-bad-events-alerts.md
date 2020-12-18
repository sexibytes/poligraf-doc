---
title: vCenter Bad Events Alerts
---

Since **[template variables are not (yet?) supported in grafana](https://github.com/grafana/grafana/issues/10412#event-1407706154)**, you can’t configure alerts on the vCenter Bad Events dashboard. So we decided to create a similar dashboard with wildcards and preconfigured alerting.

This is a first step since you’ll receive a notification for anything catched by our amazing AI but we figured that it’s **better than nothing at all**.

To get alerts, you’ll need to add and configure a notification channel in grafana and since we love **Telegram**, here is a quick how to **do it yourself**.

First [you have to create a bot and get the API token and the Chat ID](https://core.telegram.org/bots#6-botfather). Then create a new notification channel with the provided information:

![telegram_alert_0](/media/telegram_alert_0.png)

![telegram_alert_1](/media/telegram_alert_1.png)

You need to check the “Default” and the “Disable Resolve Message” boxes so this will work out of the box with our preconfigured dashboard:

![telegram_alert_2](/media/telegram_alert_2.png)

And that’s it, now you’ll received all your bad events in this telegram chat:

![telegram_alert_3](/media/telegram_alert_3.png)

![telegram_alert_4](/media/telegram_alert_4.png)
