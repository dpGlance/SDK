# Glance Mobile SDK — Test Builds

Pre-built iOS xcframework drops for customer validation.

## Releases

| Release | Tag | Description |
|---------|-----|-------------|
| [GlanceFramework 7.2 Swift 6](https://github.com/dpGlance/SDK/releases/tag/7.2_Swift6_iOS) | `7.2_Swift6_iOS` | GlanceFramework only (Swift 6) |
| [Glance SDK 7.3.0 Schwab Proxy Fix](https://github.com/dpGlance/SDK/releases/tag/7.3.0_SchwabProxyFix_SDK880) | `7.3.0_SchwabProxyFix_SDK880` | SDK-880 SecureSend crash fix — **GlanceCore + GlanceFramework** |

---

## 7.3.0 Schwab Proxy Fix (SDK-880)

**For Schwab iOS testing** — fixes `EXC_BAD_ACCESS` in `SSLSocket::SecureSend` when legacy presence TLS fails behind a corporate proxy.

**Download:** [GlanceSDK_7.3.0_SchwabProxyFix_SDK880.zip](https://github.com/dpGlance/SDK/releases/download/7.3.0_SchwabProxyFix_SDK880/GlanceSDK_7.3.0_SchwabProxyFix_SDK880.zip)

### What's in the zip

- `GlanceCore.xcframework`
- `GlanceFramework.xcframework`
- `SOURCE.txt` — build metadata and UUIDs
- `INTEGRATION.md` — integration notes

### Link both frameworks

GlanceFramework does **not** bundle GlanceCore in this drop. Add and embed **both** xcframeworks in the host app.

### Verify (arm64)

```
GlanceCore UUID:      DF0B60AD-DE32-3684-8CA6-66DA770A3B7E
GlanceFramework UUID: 1C7B45AB-8F21-3D88-9220-AB001C5E37F2
```

### Scope

Minimal hotfix only (`GSocket.cpp`, `SSLSocketA.cpp`). No presence lifecycle or reconnect behavior changes.

---

## 7.2 Swift 6

**Download:** [GlanceFramework_7.2_Swift6.xcframework.zip](https://github.com/dpGlance/SDK/releases/download/7.2_Swift6_iOS/GlanceFramework_7.2_Swift6.xcframework.zip)

GlanceFramework xcframework only.
