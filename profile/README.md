# VPN Client

[🇬🇧 English](README.md) | [🇷🇺 Русский](README_ru.md) |  [🇹🇭 ไทย](README_th.md)
---

**VPN Client** is a cross-platform VPN client supporting multiple cores and protocols.

## Key Features

- **Multi-protocol support**: Xray (VMess, VLESS, Reality, Shadowsocks, Trojan, SSH), OpenVPN, WireGuard, as well as SOCKS5/HTTP/HTTPS proxy.
- **Cross-platform**: Available for iOS, Android, macOS, Windows, and Linux.
- **High performance**: Native functionality implemented in Swift (iOS) and Kotlin (Android), and critical components written in C++ and Golang ensure speed and stability.

## Architecture

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

![VPN Client Controller](https://raw.githubusercontent.com/VPNclient/.github/refs/heads/main/assets/vpnclient_scheme2.png)

## Supported Platforms

- **iOS**
- **Android**
- **macOS**
- **Windows**
- **Linux**

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
