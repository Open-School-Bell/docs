---
title: Webhooks
parent: Configuration
---
# Webhooks

## Inbound

### Adding

Adding a new inbound webhook requires the following options.

|Option|Explination|
|:-----|:----------|
|Slug|The slug used to trigger the webhook.|
|Action|The action to trigger with this webhook.|

Once the hook is created it will be given a key that needs to be passed when calling it.

### Triggering

Trigger the webhook with a POST request to the `slug` with your key in the JSON payload.

```
curl -H 'Content-Type: application/json' -d '{"key": "YOURKEY"}' -X POST http://controller/hook/lockdown
```

If the action you are triggering with this action is a _broadcast_ action you can pass a zone in the JSON payload as well.

```
curl -H 'Content-Type: application/json' -d '{"key": "YOURKEY", "zone": "ZONEID"}' -X POST http://controller/hook/lockdown
```

## Outbound

### Adding

Adding a new outbound webhook requires the following options.

|Option|Explination|
|:-----|:----------|
|Target|The URL that will recieve the POST request.|
|Event|The event that will trigger this POST request.|

### Authenticating

When receiving the request you can use the generated key to confirm that the request came from the OSB controller.

