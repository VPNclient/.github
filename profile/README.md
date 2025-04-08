# VPN Client

[🇬🇧 English](README.md) | [🇷🇺 Русский](README_ru.md) |  [🇹🇭 ไทย](README_th.md)
---

**VPN Client** is a cross-platform VPN client supporting multiple cores and protocols.

## 🚀 Key Features

- **Multi-protocol support**: Xray (VMess, VLESS, Reality, Shadowsocks, Trojan, SSH), OpenVPN, WireGuard, as well as SOCKS5/HTTP/HTTPS proxy.
- **Cross-platform**: Available for iOS, Android, macOS, Windows, and Linux.
- **High performance**: Native functionality implemented in Swift (iOS) and Kotlin (Android), and critical components written in C++ and Golang ensure speed and stability.

## 🖥️ Supported Platforms

- ✅ iOS  
- ✅ Android  
- ✅ macOS  
- ✅ Windows  
- ✅ Linux  

## 📦 Architecture

VPN Client architecture is structured across several layers:

1. **VPNclient-engine**  
   The core engine for various platforms. Handles VPN setup and management, traffic routing, OS integration, and communication with VPN protocols (OpenVPN, WireGuard, Xray, etc.).

2. **Platform Wrappers:**
   - **[VPNclient-engine-flutter](https://github.com/VPNclient/VPNclient-engine-flutter)**  
     Flutter plugin using `MethodChannel` to interact with native code. Allows using VPNclient-engine in cross-platform Flutter apps.
   - **[VPNclient-engine-react-native](https://github.com/VPNclient/VPNclient-engine-flutter)**  
     React Native wrapper via `NativeModules`. Provides the same VPNclient-engine integration for React Native apps.

3. **VPN Client App**  
   A Flutter-based application utilizing the wrappers to manage VPN sessions and display connection status.

<details>
<summary>Architecture Diagram(click to expand)</summary>
   
```mermaid
graph TD
  style A fill:#f9d5e5
  A[VPNclient App] --> Z{UI Framework}

  Z -->|Flutter| B[Flutter Plugin]
  Z -->|React Native| C[React Native Plugin]
  Z -->|Native| D[Swift/Kotlin/C++]

  style B fill:#eeac99
  style C fill:#eeac99
  style D fill:#eeac99

  B --> E[VPNclient Engine]
  C --> E
  D --> E

  style E fill:#fbc4ab

  E --> F[iOS]
  E --> G[Android]
  E --> H[macOS]
  E --> I[Windows]
  E --> J[Linux]
```

</details>

---

## ⚙️ Supported Cores & Wrappers

- 🔌 **Xray Core** via:
  - VPNclient Xray Wrapper
  - libXray Wrapper
  - sing-box Wrapper
- 🔐 **OpenVPN Core**
- ⚡ **WireGuard Core**
  
<details>
<summary>🧠 Core Support Diagram (click to expand)</summary>

```mermaid
graph TD
  style A fill:#fbc4ab
  A[VPNclient Engine] --> B{Cores}
  style B fill:#fef9c3

  %% Wrappers
  B --> C[VPNclient Xray Wrapper]
  B --> D[libXray Wrapper]
  B --> E[sing-box Wrapper]
  style C fill:#a0c4ff
  style D fill:#a0c4ff
  style E fill:#a0c4ff

  %% Xray Core
  C --> H[Xray Core]
  D --> H[Xray Core]
  E --> H[Xray Core]
  style H fill:#a0c4ff

  %% Xray Protocols 
  H --> H1[VLESS]
  H --> H2[VMess]
  H --> H3[Reality]
  H --> H4[Shadowsocks]
  H --> H5[Hysteria]
  H --> H6[Trojan]
  style H1 fill:#a0c4ff
  style H2 fill:#a0c4ff
  style H3 fill:#a0c4ff
  style H4 fill:#a0c4ff
  style H5 fill:#a0c4ff
  style H6 fill:#a0c4ff

  %% OpenVPN Core
  B --> F[OpenVPN Core]
  F --> F1[OpenVPN]
  style F fill:#d0f4de
  style F1 fill:#d0f4de

  %% WireGuard Core
  B --> G[WireGuard Core]
  G --> G1[WireGuard]
  style G fill:#ffc6ff
  style G1 fill:#ffc6ff
```

</details>

---

## 🧦 Supported Proxy Drivers

- 🧦 VPN Client Driver
- 🧦 [hev-socks5](https://github.com/heiher/hev-socks5-tunnel)
- 🧦 tun2socks
- 🧦 WinTun

<details>
<summary>🧵 Proxy Driver Diagram (click to expand)</summary>

### Proxy Driver Diagram
```mermaid
graph TD
  style A fill:#fbc4ab
  A[VPNclient Engine] --> B{Proxy }
  style B fill:#fef9c3

  B --> C[VPN Client Driver]
  B --> D[hev-socks5]
  B --> E[tun2socks]
  B --> F[WinTun]

  style C fill:#caffbf
  style D fill:#a0c4ff
  style E fill:#ffc6ff
  style F fill:#ffd6a5
```

</details>

## Repositories

- [VPNclient-app](https://github.com/VPNclient/VPNclient-app) – Flutter app example
- [VPNclient-engine-flutter](https://github.com/VPNclient/VPNclient-engine-flutter) – Flutter Engine
- [VPNclient-engine-android](https://github.com/VPNclient/VPNclient-engine-android) – Android Engine
- [VPNclient-engine-ios](https://github.com/VPNclient/VPNclient-engine-ios) – iOS Engine
- [VPNclient-engine-windows](https://github.com/VPNclient/VPNclient-engine-windows) – Windows Engine
- [VPNclient-engine-linux](https://github.com/VPNclient/VPNclient-engine-linux) – Linux Engine

## Example Apps

- **[SuperHit-VPNclient-app](https://github.com/VPNclient/SuperHit-VPNclient-app)**
- **[fineVPN-VPNclient-app](https://github.com/VPNclient/fineVPN-VPNclient-app)**

## Benefits of VPN Client Engine

1. **System-level native integration**
2. **Flexibility**
3. **Open Source**

## Getting Started

Choose the appropriate repository for your platform from the list above and follow the instructions in that repository’s README.

## License

This project is licensed under the Extended GPLv3. See the [LICENSE](LICENSE.md) file for details.

## Contact

For more information, visit our website: [vpnclient.click](https://vpnclient.click/).













