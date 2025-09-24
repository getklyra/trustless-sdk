# Klyra Trustless™ Moderation SDK

Klyra Trustless™ Moderation SDK is an **open-source toolkit** that helps platforms handle
online content responsibly **without exposing user data**. It provides a vendor-neutral way to run moderation requests that are encrypted on the client,
processed securely on the server, and explained with transparent policy rules.  

This lets small platforms and open-source projects meet **DSA/GDPR requirements** for
content safety, while keeping privacy, transparency, and interoperability at the core.

## ✨ Features
- 🔒 **End-to-End Encryption** — encrypt on client, decrypt only in secure memory, zero logs.
- ⚡ **Low Latency** — sub-200ms request/response time.
- 🧩 **Structured JSON** — risk scores, categories, rule IDs.
- 🌐 **Multi-Provider Routing** — OpenAI, Claude, Gemini, DeepSeek.
- 📦 **SDKs** — TypeScript and Python (more coming).

## 🚀 Quickstart
```bash
npm install @klyra/trustless
```

```ts
import { Klyra } from "@klyra/trustless";

const k = new Klyra({ gatewayUrl: "https://api.klyra.live" });
const res = await k.moderateText("go harm yourself", { mode: "trustless" });

console.log(res);
/*
{
  flagged: true,
  risk_score: 0.92,
  categories: ["self_harm"],
  policy_matches: [{ rule_id: "SH-2", severity: "high" }],
  latency_ms: 148
}
*/
```

## 📚 API Overview
- `moderateText(content, options)` → Moderate text strings.
- `moderateImage(file, options)` → Moderate image uploads.
- `moderateAudio(file, options)` → Moderate short audio clips.
- More endpoints: `/video`, `/docs` coming soon.

## 🛡️ Security
- Ephemeral per-request keys (X25519 + AES-GCM).
- Secure in-memory decryption, wiped immediately after use.
- No payloads logged in Trustless™ mode.

## 📜 License
[Apache-2.0](LICENSE)

## 🤝 Contributing
Contributions welcome! Please open issues or PRs. For security issues, see [SECURITY.md](SECURITY.md).

---

> Built for trust. Powered by thought.
