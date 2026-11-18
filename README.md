# Asgard Launcher

**Asgard Launcher** is a lightweight native Windows desktop launcher (built in Rust with GPUI) published by **Asgard Studio LLC** for launching official multiplayer Minecraft: Java Edition experiences, including *Asgard: Sacred Frontier* and *GunZ*.

## Overview

- **Official Microsoft Account Sign-In Only**: Uses the standard Microsoft OAuth 2.0 Device Code Flow (`consumers` tenant, scopes `XboxLive.signin` and `offline_access`). Players sign in directly on Microsoft's official verification page (`https://www.microsoft.com/link`).
- **Legitimate Game Ownership Verification**: Exchanges the user's Microsoft token for Xbox Live and XSTS tokens, authenticates via `https://api.minecraftservices.com/authentication/login_with_xbox`, and verifies legitimate *Minecraft: Java Edition* ownership (`/entitlements/mcstore`) and player profile (`/minecraft/profile`) before launching the game. Offline/unlicensed accounts and third-party authentication servers are not supported.
- **Resource & Modpack Synchronization**: Verifies file hashes over HTTPS and synchronizes required client modpacks, resource packs, and updates in isolated game directories.
- **Local Encrypted Session Storage**: Account tokens are stored exclusively on the player's own computer in `microsoft-account.dat`, encrypted via Windows Data Protection API (DPAPI) bound to the current Windows user account. Credentials and tokens are never transmitted to Asgard Studio servers or written to logs.

## Account & Privacy

See [PRIVACY.md](./PRIVACY.md) for full details on authentication data handling, local token storage, and account removal.

- **Publisher**: Asgard Studio LLC (`30 N Gould St, Sheridan, WY 82801, United States`)
- **Support & Privacy Contact**: `s@asgard.sh`

---

*NOT AN OFFICIAL MINECRAFT PRODUCT. NOT APPROVED BY OR ASSOCIATED WITH MOJANG OR MICROSOFT.*
