# synaps-network-iframe-integration

Iframe integration of the network subdomain system

## Installation

Add the iframe element on your frontend. Generate a JWT token and replace YOUR_TOKEN by the token generated. 

Token structure :
```
{
"exp": expiration_date,
"iat": time.Now().UTC().Unix(),
"email": "user_email",
"alias": "session_alias",
}
```
## Usage

```html

<iframe  id="iframeExample"  title="Iframe Example"

allow="microphone; camera; midi; encrypted-media;"

allowtransparency="true"

allowfullscreen="true"

border="0"

frameborder="none"

resize="none"

src="https://network.synaps.io/project/holoride?token=YOUR_TOKEN">

```

## Webhooks

Account creation webhook structure :
```
{
  "session_id": synaps_session,
  "state": "CREATED",
  "email": user_email
}
```
This webhook is sent just after the account creation of a user

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