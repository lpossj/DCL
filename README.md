# DCL

## 中文

DCL 是面向 Minecraft Java 版玩家的第三方桌面启动器，优先支持 Windows 10/11 x64。界面使用 React 与 TypeScript，桌面容器为 Tauri 2，本地核心由 Rust 实现，不运行独立的常驻 HTTP 后端。

已实现的功能包括原版与 Fabric 版本安装、独立实例管理、共享依赖缓存、按需 Java 准备、Modrinth 模组资源管理及本地 `.mrpack` 导入。上述功能已进入生产编译与 Windows 安装包，下载、安装和游戏启动尚未实际运行确认。

登录代码使用 Microsoft 官方设备代码流程：显示并复制授权码，通过系统默认浏览器打开官方页面，再由本地核心完成 Microsoft、Xbox、XSTS 和 Minecraft 认证。代码会检查 Java 版游戏权益及玩家档案；没有有效权益时停止登录。DCL 不收集 Microsoft 密码，也不提供绕过认证或游戏所有权检查的功能。

刷新令牌使用 Windows 系统凭据机制保存，短期游戏访问令牌保存在进程内存。实例、配置、缓存和日志保存在本地；登录和资源获取仍需连接相应服务。无需注册 DCL 账号，当前没有广告或云同步服务。

**当前状态：** 自有应用已注册，Minecraft Java 服务 API 准入申请已于 2026-10-21 提交，等待审核。完整正版登录未实际运行确认；获准后仍需将应用配置内置到发行包。玩家无需自行申请或填写开发者参数。

DCL 安装包不附带 Minecraft 游戏本体。使用游戏需要有效的游戏授权；模组和其他资源仍受各自作者及平台的许可约束。

**DCL 并非 Minecraft 官方产品，未经 Mojang 或 Microsoft 批准，也与其无关联。**

## English

DCL is a third-party desktop launcher for Minecraft: Java Edition, with Windows 10/11 x64 as its initial target. It uses React and TypeScript, Tauri 2, and a local Rust core. It does not run a separate persistent HTTP backend.

The implementation includes vanilla and Fabric installation, isolated instances, shared dependency caches, on-demand Java preparation, Modrinth mod management, and local `.mrpack` import. Production builds and a Windows installer have been produced. Downloads, installations, and game launches have not yet been confirmed through actual operation.

The authentication code uses Microsoft's official device-code flow, copies the displayed code, and opens the official authorization page in the system's default browser. The local core then performs Microsoft, Xbox, XSTS, and Minecraft authentication and checks Java Edition entitlements and the player profile. It stops sign-in when valid entitlements are absent. DCL does not collect Microsoft passwords or provide authentication or ownership-check bypasses.

Refresh credentials use the Windows system credential mechanism; short-lived game access tokens remain in process memory. Instances, settings, caches, and logs are local, while authentication and resource retrieval require network access. No DCL account registration is required. The current application has no advertising or cloud synchronization service.

**Current status:** DCL's own application has been registered. Its Minecraft Java Game Service API access request was submitted on October 21, 2026 and is awaiting review. End-to-end official-account sign-in has not been confirmed in actual operation. API approval and a release with embedded application configuration are still pending; players do not need to register an application or enter developer settings.

The DCL installer does not include the Minecraft game itself. A valid game license is required. Mods and other resources remain subject to their authors' and platforms' respective licenses.

**NOT AN OFFICIAL MINECRAFT PRODUCT. NOT APPROVED BY OR ASSOCIATED WITH MOJANG OR MICROSOFT.**

---

维护者 / Maintainer: **lpossj**

联系邮箱 / Contact: [2106841308@qq.com](mailto:2106841308@qq.com)
