# SecureNode — Device-Level Call Identity & Branding

SecureNode helps enterprises and platforms improve **call trust** by showing verified identity information (brand name, optional logo, optional call context) **directly on the recipient’s device** when a call is received.

SecureNode operates **outside the carrier and SIP voice path**:
- Calls are still routed by your existing carrier/CPaaS stack.
- SecureNode does not route calls or process call audio.
- Branding is applied at the device level using native mobile capabilities.

## Branded call experience (example)

![SecureNode Call Branding Preview](https://assets.zyrosite.com/cdn-cgi/image/format=auto,w=1440,h=957,fit=crop/mv02wLOOE4skoDMe/call-branding-preview-nbgyYSlE9LSVX1N6.png)

## What you can build with it

- Branded inbound caller identity for large outbound programs (contact centres, healthcare, logistics, fintech, utilities)
- Multi-app deployments where you control identity centrally but display it consistently on devices
- Privacy-forward identity delivery (minimal metadata, cached locally for instant display)

## How teams use SecureNode (typical flow)

1. **Get portal access**
2. **Create API keys** for your client applications in the portal (API Access page).
3. **Download reference apps** (optional) to validate the experience end-to-end:
   - `https://verify.securenode.io/sdk#sdk-downloads`
4. **Integrate the SDK** into your mobile app(s):
   - Your app authenticates using `X-API-Key`.
   - Devices sync identity metadata and cache it locally for fast, offline-capable display.
5. **Roll out to production** in stages (pilot → region/team → full deployment).

## Platform architecture overview

![SecureNode Call Verification & API Architecture](https://assets.zyrosite.com/cdn-cgi/image/format=auto,w=2800,h=1297,fit=crop/mv02wLOOE4skoDMe/securenode-branded-call-verification-api1-ACntv4FdjFkFWdy1.png)

## Public API (high level)

- **Base URL**: `https://verify.securenode.io`
- **Auth**: send `X-API-Key` on each request
- **Core endpoints**: branding sync + lookup, and device register/update for device attribution/state

## Notes for large projects

- **Separate keys per app**: treat API keys as per-environment and per-app credentials.
- **Design for retries + offline**: callers arrive when networks are unreliable; rely on sync + local cache for consistent UX.
- **Operational ownership**: align product, mobile, and security teams on what identity is displayed and when.

## Contact

To discuss partnerships, integrations, or early access:

- **Email**: admin@securenode.io
- **Web**: `https://securenode.io`

© SecureNode. All rights reserved.
