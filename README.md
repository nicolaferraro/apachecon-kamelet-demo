# ApacheCon Kamelet Demo

This demo creates a scenario where data from Twitter is mixed with other customer data (from Beer Source) and finally sent into a Telegram chat.

The original presentation shows how to create the beer-source Kamelet and how to contribute it to the Apache Catalog.

# Preparing

Edit the following files:

- `02.channel-to-telegram.yaml`: Add the authorization token of your chat bot (ask the [@BotFather](https://telegram.me/BotFather)) and destination chat ID;
- `02.twitter-to-channel.yaml`: Enter all the tokens of your application from the [Twitter developer portal](https://developer.twitter.com/en/portal/apps).

## Running

Have your OpenShift or Kubernetes running with [Camel K properly installed](https://camel.apache.org/camel-k/latest/installation/installation.html).

```
for f in *.yaml; do k apply -f $f; done
```

Watch your Telegram app.
