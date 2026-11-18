# Privacy Policy — Asgard Launcher

*Last updated: November 18, 2026*

**Asgard Launcher** is developed and operated by **Asgard Studio LLC** (`30 N Gould St, Sheridan, WY 82801, United States`). This Privacy Policy explains what data Asgard Launcher accesses, how Microsoft authentication is handled, and how data is stored on your device.

## 1. Microsoft Authentication & Passwords

- Asgard Launcher uses Microsoft's official **OAuth 2.0 Device Code Flow**. You enter your code and sign in directly on Microsoft's official webpage (`https://www.microsoft.com/link`) in your own browser.
- **Asgard Launcher never sees, collects, processes, or stores your Microsoft account email address, password, or two-factor authentication credentials.**

## 2. Minecraft Services API Usage

After you authorize sign-in with Microsoft, Asgard Launcher communicates directly from your device with official Microsoft, Xbox Live, and Minecraft Services endpoints (`api.minecraftservices.com`) solely to:

1. Obtain an Xbox Live token, XSTS token, and Minecraft access token (`login_with_xbox`);
2. Verify legitimate *Minecraft: Java Edition* license ownership (`/entitlements/mcstore`);
3. Retrieve your Minecraft profile username and UUID (`/minecraft/profile`) required to launch the game client locally.

## 3. Local Token Storage & Security

- Refresh tokens and Minecraft session tokens are stored **exclusively on your local computer** inside `microsoft-account.dat`.
- The entire `microsoft-account.dat` file is encrypted at rest using the **Windows Data Protection API (DPAPI)** bound to your current Windows user profile, making it unreadable on any other machine or user account.
- **Zero Server Upload**: Authentication tokens are never transmitted to Asgard Studio LLC servers, never shared with third parties, and never printed in application logs.

## 4. Data Deletion & Sign-Out

- Clicking **Sign Out** inside Asgard Launcher immediately and permanently deletes the local `microsoft-account.dat` session file from your device.
- You may also revoke Asgard Launcher's access at any time from your Microsoft Account permissions page (`https://account.microsoft.com/privacy/app-access`).

## 5. Network Requests

Aside from official Microsoft/Mojang authentication endpoints, Asgard Launcher connects over HTTPS to official distribution CDNs solely to check launcher updates and verify/download game resource packs. No personal browsing data or advertising identifiers are collected.

## 6. Contact

For privacy inquiries or support requests, contact:

- **Entity**: Asgard Studio LLC
- **Address**: 30 N Gould St, Sheridan, WY 82801, United States
- **Email**: `s@asgard.sh`

---

*NOT AN OFFICIAL MINECRAFT PRODUCT. NOT APPROVED BY OR ASSOCIATED WITH MOJANG OR MICROSOFT.*
