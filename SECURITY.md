# Security Policy

## 🔒 Supported Versions
This project is currently in **alpha**. Only the latest commit on `main` is supported for security patches.

## 📢 Reporting a Vulnerability
If you discover a security issue:
- **Do not open a public GitHub issue.**
- Email us directly at **security@klyra.live**.
- Include a description of the vulnerability, steps to reproduce, and potential impact.

We aim to acknowledge reports within **72 hours**, provide an assessment within **7 days**, and patch critical issues as soon as possible.

## 🔑 Scope
- Client SDKs (TypeScript, Python) implementing Trustless™ mode.
- Reference Gateway (Node/Rust) for secure in-memory decryption.
- JSON schemas and policy engine components.

## 🧪 Out of Scope
- Issues in upstream providers (OpenAI, Claude, Gemini, DeepSeek).
- End-user applications built on top of Klyra.
- Dependencies not bundled in the SDK.

## 🛡️ Security Practices
- Ephemeral per-request keys (X25519 + AES-GCM).
- Secure memory handling with zeroization.
- Continuous integration with security linting & dependency scanning.
- Planned external audit before v1.0.

## 📜 Disclosure
We follow **coordinated disclosure**: please give us reasonable time to patch before sharing publicly. Researchers will be credited in release notes if desired.
