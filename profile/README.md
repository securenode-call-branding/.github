# SecureNode Portal & API

> **Verified Caller Identity & Call Branding Platform**  
> Native. Offline-first. OS-compliant.

<p align="center">
  <img
    src="https://assets.zyrosite.com/mv02wLOOE4skoDMe/securenode_p-VJEjTb63yD2sHE66.jpg"
    alt="SecureNode Call Branding Preview"
    width="420"
    style="border: none; box-shadow: none;"
  />
</p>

SecureNode provides a platform and SDKs for **verified caller identity and call branding**, designed to integrate cleanly with native mobile operating systems **without replacing the call UI or intercepting audio**.

This repository contains the **SecureNode Portal**, public API definitions, and developer documentation used to integrate SecureNode into mobile applications and enterprise systems.

---

## 🚀 What SecureNode Does

- Displays **verified brand identity** on incoming calls
- Uses the **native OS call experience** (no custom dialer)
- Resolves identity **locally and offline**
- Syncs approved branding data in the background
- Reports usage **after the call**, never during it

SecureNode is **not** a VoIP platform, dialer replacement, or call recording system.

---

## 🧠 Core Principles

- **Local-first** – No network dependency at call time
- **OS-compliant** – Works within Android & iOS constraints
- **Non-intrusive** – No audio access, no UI replacement
- **Predictable billing** – Pay only for value delivered
- **Enterprise-ready** – Auditable, secure, and scalable

---

## 📦 Repository Structure


> Documentation in `/docs` is designed to be consumable by tools such as Mintlify.

---

## 🔌 Platform Components

### Portal
- Company & user management
- Branding profiles & approval workflow
- Device visibility & diagnostics
- Usage & billing overview
- Debug & support tooling

### API
- REST-based integration
- Stable, backward-compatible contracts
- OpenAPI definitions provided
- Designed for async, event-driven usage

### Mobile SDKs
- Android SDK (reference implementation)
- iOS SDK (CallKit-safe)
- Local cache + background sync model
- No runtime network dependency for call handling

---

## 📲 Incoming Call Flow (High-Level)


If no branding is available, the call behaves exactly as it would without SecureNode.

---

## 💳 Billing Model (Transparent by Design)

SecureNode uses a **base + overage** billing model:

- **Monthly platform access fee**
- **Included monthly imprint allowance**
- **Usage-based overage** (only when branding is displayed)

### What is billable
- ✅ A call where verified branding is displayed

### What is NOT billable
- ❌ Device syncs
- ❌ Lookups
- ❌ API calls
- ❌ Debug or demo activity
- ❌ Failed or unsupported matches

Billing is handled via **Stripe**, with all usage enforcement performed server-side.

---

## 🧪 “Try It” Tools

The portal includes a **Try It / Simulation panel** that allows developers to:
- Test branding lookups
- Preview outcomes
- Validate configuration
- Understand billing behavior safely

No production usage is generated from simulation tools.

---

## 🔐 Security & Compliance

- No call audio interception
- No VoIP or dialer replacement
- OS permission-aware
- App Store & Play Store compliant
- Privacy-first architecture

SecureNode is designed for **enterprise, regulated, and high-trust environments**.

---

## 🧑‍💻 Getting Started

1. Create a SecureNode account
2. Generate an API key
3. Register a device via the SDK
4. Configure branding profiles
5. Sync and test using the portal
6. Go live

See `/docs` for step-by-step integration guides.

---

## 📄 Documentation

- SDK architecture & expectations
- API reference (OpenAPI)
- Billing & metering rules
- Android ↔ iOS parity guidelines
- App Store compliance notes

All documentation lives in `/docs`.

---

## 🤝 Support & Contribution

This repository is maintained by the SecureNode team.

For:
- Integration support
- Enterprise onboarding
- Security inquiries

Please contact your SecureNode representative or use the official support channels.

---

## 📜 License

Copyright © SecureNode.  
All rights reserved.

This repository is provided for integration and evaluation purposes under the applicable SecureNode agreements.

This software is provided for evaluation and integration testing only.
No production use, modification, distribution, or commercial deployment
is permitted without an executed SecureNode commercial license agreement.

Unauthorized use constitutes copyright infringement.

