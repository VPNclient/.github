[![Telegram Channel](https://img.shields.io/endpoint?label=Channel&style=flat-square&url=https%3A%2F%2Ftg.sumanjay.workers.dev%2Fvpnclient_support&color=blue)](https://t.me/vpnclient_support)

# VPN Client

Основная идея заключается в вынесении функционала, отвечающего за работу с VPN соединением в отдельный контроллер.
В контроллере присутствуют сервисы и логика.
Сервисы
* Открывают системное VPN соединение
* Работают с драйвером виртуальной сетевой карты, отправляя пакеты в локальный socks (tun2socks или hev-socks5)
* Туннелируют данные из локального socks в VPN ноду (LibXray, Sing-Box)

![VPN Client Controller](https://raw.githubusercontent.com/VPNclient/.github/refs/heads/main/assets/vpnclient_scheme2.png)


https://github.com/VPNclient/VPNclient-app - репозиторий примера приложения на Flutter

https://github.com/VPNclient/VPNclient-engine-flutter - VPN Client Engine на Flutter

https://github.com/VPNclient/VPNclient-engine-android - VPN Client Engine для Android 

https://github.com/VPNclient/VPNclient-engine-ios - VPN Client Engine для iOS 

https://github.com/VPNclient/VPNclient-engine-windows - VPN Client Engine для Windows 

https://github.com/VPNclient/VPNclient-engine-linux - VPN Client Engine для Linux

Примеры форков прототипов для заказчиков:

https://github.com/VPNclient/SuperHit-VPNclient-app - Super Hit

https://github.com/VPNclient/fineVPN-VPNclient-app - fineVPN.org

## Преимущества решений на базе OpenSource VPN Client Engine
### 🖥️ 1. Технические преимущества решения
#### 🛠️ Системная нативность
- **Высокая производительность:**  Вся логика и службы по работе с VPN соединением вынесена на нативные языки, а не на Flutter. Критически важные функции, такие как маршрутизация трафика, автовыбор серверов и пропинговка, реализованы на нативных языках (Swift для iOS, Kotlin для Android), что обеспечивает максимальную производительность, стабильность и остуствие лагов.

#### 📱 Кросс-платформенность интерфейса
- **Единая кодовая база:** UI и пользовательские функции реализованы на Flutter, что позволяет легко адаптировать её для разных платформ (iOS, Android, Windows, macOS, Unix).

#### 🔄 Упрощенная интеграция с кастомными API
- **Гибкость:** Логика взаимодействия с вашим API (Авторизация, оплаты, ...) реализована на Flutter, что позволяет быстро и легко адаптировать её под ваши нужды без необходимости изменять нативный код.

#### 🛡️ Безопасность и стабильность
- **Надежность:** Нативные компоненты контроллера обеспечивают стабильную работу критически важных функций, таких как управление VPN-соединениями и маршрутизация трафика. 


### 🛡️ 2. Защита от зависимости от одного разработчика
- **OpenSource защищает от рисков**, связанных с потерей доступа к исходному коду или разработчикам. Если основной разработчик перестанет поддерживать проект, сообщество или другие специалисты смогут продолжить работу.

### 🛠️ 3. Возможность самостоятельной доработки
- Вы можете самостоятельно вносить изменения в код, добавлять новые функции или исправлять ошибки без необходимости ждать поддержки от основной команды.

### 🌍 4. Поддержка сообщества
- OpenSource проекты развиваются благодаря вкладу множества разработчиков. Это означает, что вы получаете регулярные обновления, исправления и новые функции.

### 🔄 5. Гибкость в использовании
- Вы можете использовать оригинальную версию OpenSource или создать свою ветку (форк) с уникальными изменениями.

### ⚡ 6. Быстрая реакция на изменения
- Если в OpenSource решение вносятся улучшения (например, поддержка новых протоколов или исправление уязвимостей), вы можете быстро интегрировать эти изменения в свой проект.

### 🎨 7. Возможность кастомизации
- Вы можете добавлять уникальные функции, которые не будут доступны в основной версии OpenSource. Например, интеграция с вашим API, кастомная маршрутизация трафика или уникальные элементы интерфейса.

### 🔄 8. Поддержка обновлений
- Вы можете самостоятельно обновлять свою версию OpenSource, интегрируя новые функции и исправления из основной ветки.

### ⚠️ 9. Минимизация рисков
- OpenSource решения менее подвержены рискам, связанным с прекращением поддержки или банкротством компании-разработчика.

### 🔍 10. Прозрачность и безопасность
- OpenSource код открыт для проверки, что позволяет убедиться в отсутствии скрытых уязвимостей или нежелательных функций.

### 💼 11. Гибкая лицензия
- OpenSource VPN Client Controller позволяет использовать решение бесплатно для некоммерческих проектов или небольших стартапов. Для коммерческого использования предлагаются прозрачные условия лицензирования.

### 🏁 Итог:
OpenSource VPN Client Controller — это надежное, гибкое и экономически выгодное решение для создания VPN-приложений. Вы получаете полный контроль над кодом, возможность кастомизации и поддержку сообщества, что делает его идеальным выбором для бизнеса.
