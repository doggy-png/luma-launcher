# Luma Launcher

Luma is an independent Windows x64 desktop launcher demo for Minecraft: Java Edition. It currently targets version 1.8.9, with separate vanilla and Forge instances and a translucent desktop interface.

**Development status:** version 0.1.2 is a demo. Microsoft and Xbox authentication succeeded in a real test, but Minecraft's login service rejected the application with HTTP 403, `Invalid app registration`. Minecraft API access has not been approved, and end-to-end game sign-in has not yet been validated. This page does not claim official approval or a working release.

## Features in development

- Microsoft account sign-in in the system browser, with authorization-code flow, PKCE and a local desktop callback.
- Authenticated Minecraft profile retrieval and skin viewing or updating through the official services.
- Java runtime support, separate 1.8.9 vanilla and Forge instances, and configurable game settings.
- Compatible mod discovery and installation through Modrinth, with dependency handling and file integrity checks.
- Local shader and resource-pack importing.
- A built-in client for a self-hosted multiplayer relay. No public relay service is provided.
- Glass, acrylic and solid-color appearance options designed for a resizable desktop window.

The PvP workspace contains saved configuration presets. It does not include Badlion's proprietary client, and those presets alone do not install or implement all PvP mods.

## Authentication and API purpose

Luma requests Minecraft game-service API access to exchange a valid Xbox identity for a Minecraft session, retrieve the user's Java Edition profile and skin information, and apply skin changes explicitly requested by the signed-in user.

Sign-in takes place on Microsoft's official pages. Luma does not collect Microsoft passwords. The desktop client uses PKCE without a client secret. Game launch requires a valid authenticated Minecraft profile; the demo does not offer an offline authentication bypass.

The current application registration is named **Luma Launcher**, with public Client ID `ad741dfd-7573-4e59-bd2b-768a1ebe44ee`. Registration alone does not establish Minecraft API approval.

## Local data

Launcher settings and game-instance files remain in the user's local data folder. Saved account tokens use Windows-backed encryption. The diagnostic file records only a timestamp, public Client ID, outcome and a classified service error; it does not include tokens or authorization codes. Mod downloads, sign-in and an optional user-configured relay communicate with their respective providers.

## Validation and limitations

The project has 24 passing automated checks covering launcher configuration, OAuth handling, diagnostic classification, package validation, mod handling and relay behavior. Real Java and compatible mod downloads, game-file preparation, and local relay traffic have been checked. These checks do not establish successful gameplay, skin synchronization, cross-network multiplayer or improved in-game FPS.

## 繁體中文簡介

Luma 是 Windows x64 的 Minecraft Java 版啟動器 Demo，目前針對 1.8.9 原版與 Forge。提供透明玻璃桌面介面、Microsoft 正版登入流程、模組搜尋、資源包匯入、遊戲設定與可自行部署的聯機中繼。

目前 Microsoft 與 Xbox 驗證已通過；Minecraft 服務回覆 HTTP 403、`Invalid app registration`，需要申請應用存取資格。尚未完成 Minecraft 角色登入、實際遊玩與皮膚同步驗收。此專案頁只介紹開發中的功能與現況。

Luma is not an official Minecraft product and is not approved by or associated with Mojang or Microsoft. It is also independent of Badlion and Apple. Minecraft is a trademark of Mojang/Microsoft.
