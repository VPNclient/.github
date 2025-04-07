# VPN Client

**VPN Client** — это кросс-платформенный клиент VPN с поддержкой множества ядер и протоколов. 

## Основные возможности

- **Поддержка нескольких протоколов**: Xray (VMess, VLESS, Reality, Shadowsocks, Trojan, SSH), OpenVPN и WireGuard, а так же SOCKS5/HTTP/HTTPS proxy.
- **Кросс-платформенность**: Доступен для iOS, Android, macOS, Windows и Linux.
- **Высокая производительность**: Реализация нативных функций на Swift для iOS и Kotlin для Android, а так же реализация критически важных функций на C++ и Golang обеспечивает высокую скорость и стабильность работы.

## Архитектура

Архитектура VPN Client разделена на несколько уровней:

1. **VPNclient-engine**  
   Движок для разных платформ. Отвечает за установку и управление VPN-соединениями, маршрутизацию трафика, интеграцию с ядром системы и взаимодействие с VPN-протоколами (OpenVPN, WireGuard, Xray и др.).

2. **Платформенные обёртки:**
   - **[VPNclient-engine-flutter](https://github.com/VPNclient/VPNclient-engine-flutter)**  
     Плагин для Flutter, использующий `MethodChannel` для связи с нативной частью. Позволяет использовать VPNclient-engine в кросс-платформенных приложениях на Flutter.
   - **[VPNclient-engine-react-native](https://github.com/VPNclient/VPNclient-engine-flutter)**  
     Обёртка для React Native через `NativeModules`. Обеспечит аналогичную интеграцию с VPNclient-engine для приложений на React Native.

3. **VPN Client App**  
   Приложение, построенное на Flutter, использующее обёртки для управления VPN-сессиями и отображения статуса соединения.
   
![VPN Client Controller](https://raw.githubusercontent.com/VPNclient/.github/refs/heads/main/assets/vpnclient_scheme2.png)

## Поддерживаемые платформы

- **iOS**
- **Android**
- **macOS**
- **Windows**
- **Linux**

## Репозитории


https://github.com/VPNclient/VPNclient-app - репозиторий примера приложения на Flutter

https://github.com/VPNclient/VPNclient-engine-flutter - VPN Client Engine на Flutter

https://github.com/VPNclient/VPNclient-engine-android - VPN Client Engine для Android 

https://github.com/VPNclient/VPNclient-engine-ios - VPN Client Engine для iOS 

https://github.com/VPNclient/VPNclient-engine-windows - VPN Client Engine для Windows 

https://github.com/VPNclient/VPNclient-engine-linux - VPN Client Engine для Linux

## Примеры приложений
- **[SuperHit-VPNclient-app](https://github.com/VPNclient/SuperHit-VPNclient-app)**
- **[fineVPN-VPNclient-app](https://github.com/VPNclient/fineVPN-VPNclient-app)**


## Преимущества использования VPN Client Engine

1. **Системная нативность**
2. **Гибкость**
3. **Открытый исходный код**

## Начало работы

Для начала работы с VPN Client выберите соответствующий репозиторий для вашей платформы из списка выше и следуйте инструкциям в README данного репозитория.

## Лицензия

Этот проект лицензирован под лицензией Extended GPLv3. Подробности см. в файле [LICENSE](LICENSE.md).

## Контакты

Для получения дополнительной информации посетите наш сайт: [vpnclient.click](https://vpnclient.click/).

