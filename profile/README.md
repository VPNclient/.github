# VPN Client

Онсовная идея заключается в вынесении функционала, отвечающего за работу с VPN соединением в отдельный контроллер.
В контроллере присутствуют сервисы и логика.
Сервисы
* Открывают системное VPN соединение
* Работают с драйвером виртуальной сетевой карты, отправляя пакеты в локальный socks (tun2socks или hev-socks5)
* Туннелируют данные из локального socks в VPN ноду (LibXray, Sing-Box)

![VPN Client Controller](https://raw.githubusercontent.com/VPNclient/.github/refs/heads/main/assets/vpnclient_scheme.png)


[https://github.com/VPNclient/VPNclient-controller] - репозиторий контроллера

[https://github.com/VPNclient/VPNclient-controller-flutter] - обертка контроллера во flutter
