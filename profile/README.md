# VPN Client

Онсовная идея заключается в вынесении функционала, отвечающего за работу с VPN соединением в отдельный контроллер.
В контроллере присутствуют сервисы и логика.
Сервисы
* Открывают системное VPN соединение
* Работают с драйвером виртуальной сетевой карты, отправляя пакеты в локальный socks (tun2socks или hev-socks5)
* Туннелируют данные из локального socks в VPN ноду (LibXray, Sing-Box)

![VPN Client Controller](https://raw.githubusercontent.com/VPNclient/.github/refs/heads/main/assets/vpnclient_scheme2.png)


https://github.com/VPNclient/VPNclient-international - репозиторий примера приложения на Flutter

https://github.com/VPNclient/VPNclient-controller-ios - репозиторий контроллера для iOS

https://github.com/VPNclient/VPNclient-controller-android - репозиторий контроллера для Android

https://github.com/VPNclient/VPNclient-controller-flutter - обертка(wrapper) контроллера во Flutter 
