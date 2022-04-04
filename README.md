# synaps-network-iframe-integration

Iframe integration of the network subdomain system

## Usage

```html

<iframe  id="iframeExample"  title="Iframe Example"

allow="microphone; camera; midi; encrypted-media;"

allowtransparency="true"

allowfullscreen="true"

border="0"

frameborder="none"

resize="none"

src="https://bhnetwork.synaps.me">

```

## Webhooks

Verification step webhook structure :
```
{
  "session_id": synaps_session,
  "state": "VALIDATED",
  "step_id": "5994",
  "service": "LIVENESS"
}
```
This webhook is sent after each status update from the verification flow