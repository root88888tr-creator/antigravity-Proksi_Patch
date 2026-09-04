<div align="center">

<img src="icon.jpg" width="128" alt="ProksiFi Logo" style="border-radius: 24px;" />

# ProksiFi (antigravity-Proksi_Patch)

**Легковесный клиент маршрутизации и шлюз для Google Antigravity, YouTube и Discord на Windows.**

[![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011-0078D6?logo=windows&logoColor=white)](https://github.com/root88888tr-creator/antigravity-Proksi_Patch)
[![Telegram Channel](https://img.shields.io/badge/Telegram-@antigravity__proxy-2CA5E0?logo=telegram&logoColor=white)](https://t.me/antigravity_proxy)
[![Core](https://img.shields.io/badge/Engine-Mihomo%20Core-00C7B7)](https://github.com/MetaCubeX/mihomo)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

[**Скачать релиз (Proksi_Patch_Setup.exe)**](https://github.com/root88888tr-creator/antigravity-Proksi_Patch/releases/latest) • [**Telegram-канал**](https://t.me/antigravity_proxy)

</div>

---

### Основные возможности

* **Google Antigravity & AI Studio:** стабильное подключение к европейскому шлюзу (Франкфурт), предотвращающее смену региона аккаунтов на неподдерживаемый.
* **YouTube без буферизации:** автоматическая фильтрация QUIC (UDP 443) с мгновенным переключением на TCP TLS 1.3 в туннеле.
* **Discord & Telegram:** маршрутизация голосовых шлюзов, медиа-серверов и чатов в обход локальных сетевых ограничений.
* **Zero Anti-Cheat Conflicts:** не используются драйверы уровня ядра (`wintun.sys` / `WinDivert.sys`). Античиты игр (BattlEye, EasyAntiCheat, Vanguard, VAC) работают в штатном режиме без перехвата пакетов.
* **Split Tunneling:** локальный трафик (банки, Госуслуги, VK, Яндекс, маркетплейсы и онлайн-игры) идёт напрямую через вашего провайдера на максимальной скорости.
* **OTA-обновления:** маршруты и списки блокировок синхронизируются в фоне с сервером без необходимости переустанавливать приложение.

---

### Схема маршрутизации

```mermaid
graph LR
    User[Клиент Windows] -->|Antigravity / Google AI / YouTube / Discord| Gateway[Шлюз Франкфурт 🇩🇪]
    Gateway --> Internet[Целевые сервисы]
    
    User -->|Steam / Игры / Банки / Сайты РФ| Direct[Прямой домашний канал]
```

---

### Системные требования

* **ОС:** Windows 10 / Windows 11 (x64)
* **Права:** Права администратора **не требуются** (программа работает в пространстве пользователя)
* **Сеть:** Доступ к портам 443 и 7979

---

### Установка

1. Скачайте актуальный бинарник [`Proksi_Patch_Setup.exe`](https://github.com/root88888tr-creator/antigravity-Proksi_Patch/releases/latest).
2. Запустите файл и выберите необходимые компоненты маршрутизации.
3. Нажмите **«Установить и применить»**.
4. Программа автоматически создаст рабочий профиль в `%APPDATA%\ProksiFi` и разместит иконку управления в системном трее возле часов.

---

### Управление через трей

После установки в панели задач появляется иконка статуса:
* **Зелёный индикатор:** прокси-клиент активен, порт готов к передаче пакетов.
* **Серый индикатор:** системный прокси отключен, весь трафик идёт напрямую через провайдера.
* Меню по правому клику позволяет временно отключить туннелирование, выполнить проверку OTA-обновлений или полностью закрыть приложение.

---

### Удаление

Для удаления приложения достаточно:
1. Выбрать **«Выход»** в контекстном меню трея (сетевой стек Windows автоматически сбросится в исходное состояние).
2. Удалить рабочую директорию: `%APPDATA%\ProksiFi`.

---

<div align="center">
  <sub>Лицензия MIT. Разработано для сообщества.</sub>
</div>
