<div align="center">

# <img src="https://cdn-icons-png.flaticon.com/128/5968/5968756.png" height=28 /> <a href="https://github.com/calmaeromancerextol/">calmaeromancerextol</a><a href="https://github.com/calmaeromancerextol/zapret-discord-youtube">/zapret-discord-youtube</a> <img src="https://cdn-icons-png.flaticon.com/128/1384/1384060.png" height=28 />

**NEW**: Ускорение Telegram Desktop - https://github.com/calmaeromancerextol/tg-ws-proxy  
Альтернатива https://github.com/bol-van/zapret-win-bundle  
Также вы можете материально поддержать оригинального разработчика zapret [тут](https://github.com/bol-van/zapret?tab=readme-ov-file#%D0%BF%D0%BE%D0%B4%D0%B4%D0%B5%D1%80%D0%B6%D0%B0%D1%82%D1%8C-%D1%80%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%87%D0%B8%D0%BA%D0%B0)
</div>

> [!CAUTION]
> ### ФЕЙКИ
> Я не веду никакие другие страницы/группы в телеграм/ютуб каналы  
> Если вы наткнулись на что-то вне этой страницы гитхаба, что распространяется от моего лица - **ФЕЙК**.

> [!IMPORTANT]
> Все исполняемые и системные файлы в папке [`bin`](./bin) взяты из [zapret-win-bundle/zapret-winws](https://github.com/bol-van/zapret-win-bundle/tree/master/zapret-winws) и [zapret/releases](https://github.com/bol-van/zapret/releases). Вы можете это проверить с помощью хэшей/контрольных сумм.
>
> #### Проверяйте, что запускаете, используя сборки из интернета, и не используйте Яндекс Поиск! Он часто предлагает вредоносы по первым ссылкам, а настоящий репозиторий скрыт.  

> [!WARNING]
> ### АНТИВИРУСЫ
> WinDivert может вызвать реакцию антивируса.  
> WinDivert - это инструмент для перехвата и фильтрации трафика, необходимый для работы zapret.
> Он может использоваться как хорошими, так и плохими программами, но сам по себе не является вирусом.
>
> **Выдержка из [`readme.md`](https://github.com/bol-van/zapret-win-bundle/blob/master/readme.md#%D0%B0%D0%BD%D1%82%D0%B8%D0%B2%D0%B8%D1%80%D1%83%D1%81%D1%8B) репозитория [bol-van/zapret-win-bundle](https://github.com/bol-van/zapret-win-bundle)*
>
> Некоторые антивирусы склонны относить файлы WinDivert к классам повышенного риска или хакерским инструментам. Происходит удаление файла и помещение его в карантин. При этом детект обязательно имеет название `WinDivert` или `Not-a-virus:RiskTool.Multi.WinDivert`
>
> Добавьте папку с запретом в исключения антивируса, либо отключите детектирование PUA (потенциально нежелательных приложений). Например, в касперском есть галочка "Обнаруживать легальные приложения, которые злоумышленники часто используют для нанесения вреда". При аккуратной и правильной настройке исключений - рекомендуется настроить исключение, но если вы не до конца понимаете что делаете - рекомендуется отключить детект PUA.

---

## ⚙️ Пошаговое использование

1. **Включите Безопасный DNS (Secure DNS):**
    * В Chrome - "Использовать безопасный DNS", и выбрать поставщика услуг DNS (выбрать вариант, отличный от варианта "Поставщик по умолчанию")[cite: 1]
    * В Firefox - "DNS через HTTPS", выбрать режим "Персональный", затем "Выбрать провайдера/поставщика" и вписать URL поставщика вручную. Например, можно использовать `https://dns.google/dns-query` (т.к. поставщик Cloudflare может быть заблокирован)[cite: 1]
    * В Windows 11 поддерживается включение Secure DNS прямо в настройках ОС - [инструкция тут](https://remontka.pro/dns-over-https-windows-11/). Рекомендуется, если вы пользуетесь Windows 11[cite: 1]
    * Если у вас роутер Keenetic, включите в настройках роутера опцию "Транзит запросов". Отключение этой опции может привести к проблемам при настройке и использовании Secure DNS на компьютере[cite: 1]

2. **Скачайте архив** (zip/rar) со [страницы последнего релиза](https://github.com/calmaeromancerextol/zapret-discord-youtube/releases/latest)[cite: 1]

3. **Разблокируйте архив:** зайдите в свойства скачанного архива и поставьте галочку "Разблокировать". Если вы используете архиватор 7-Zip или PeaZip, этот шаг можно пропустить[cite: 1]

4. **Распакуйте** содержимое архива по пути, который **не содержит кириллицу/спец. символы**[cite: 1]

5. **Запустите нужный файл:**[cite: 1]
    * Узнать рабочую стратегию: **`service.bat`** -> `Run Tests` -> `Standard tests` -> `All configs`[cite: 1]
    * Поставить на автозапуск: **`service.bat`** -> `Install Service` -> *Выбираете подходящую стратегию*[cite: 1]

---

## ℹ️ Краткие описания файлов

- [**`general.bat ...`**](./general.bat) — запуск стратегии вручную (используется для проверки работоспособности. Пробуйте разные стратегии — ALT, FAKE и другие, пока не найдёте рабочее решение)[cite: 1]
- [**`service.bat`**](./service.bat) — установка в автозапуск и управление функциями:[cite: 1]
  - <ins>**`Install Service`** — установка любой стратегии в автозапуск (services.msc)</ins>[cite: 1]
  - **`Remove Services`** — удаление стратегии и WinDivert из служб[cite: 1]
  - **`Check Status`** — проверка статуса обхода и служб[cite: 1]
  - **`Game Filter`** — переключение режима обхода для игр (требуется перезапуск стратегии)[cite: 1]
  - **`IPSet Filter`** — переключение режима обхода сервисов из `ipset-all.txt` (`none` / `loaded` / `any`)[cite: 1]
  - **`Auto-Update Check`** — Вкл/Выкл автопроверку обновлений[cite: 1]
  - **`Replace active fakes`** — замена используемого фейка[cite: 1]
  - **`Update IPSet List`** — обновление списка `ipset-all.txt`[cite: 1]
  - **`Update Hosts File`** — обновление файла hosts <ins>**для починки веб-версии Телеграма и подключения к голосовому чату Discord**</ins>[cite: 1]
  - **`Check for Updates`** — проверка обновлений[cite: 1]
  - **`Run Diagnostics`** — диагностика проблем (в конце можно очистить кэш <img src="https://cdn-icons-png.flaticon.com/128/5968/5968756.png" height=11 /> `Discord`)[cite: 1]
  - **`Run Tests`** — проверка стратегий через `Standard tests` и `DPI checkers`[cite: 1]

---

## 🗒️ Добавление адресов прочих ресурсов

Список адресов для обхода можно расширить, добавляя их в:[cite: 1]
- **`list-general-user.txt`** — для доменов (поддомены учитываются автоматически)[cite: 1]
- **`list-exclude-user.txt`** — для исключения доменов[cite: 1]
- **`ipset-all.txt`** — для IP и подсетей[cite: 1]
- **`ipset-exclude-user.txt`** — для исключения IP и подсетей[cite: 1]
  > *Файлы `*-user.txt` создаются автоматически при первом запуске.*[cite: 1]

---

## ☑️ Частые вопросы и проблемы (FAQ)

<details>
<summary><b>После запуска скрипта general* ничего не происходит</b></summary>

После запуска стратегии должен открыться `winws.exe`, который виден в панели задач. Если этого не произошло, см. [#522](https://github.com/calmaeromancerextol/zapret-discord-youtube/issues/522).[cite: 1]
</details>

<details>
<summary><b>Ни одна стратегия не подходит</b></summary>

1. Запустите командную строку от имени администратора.[cite: 1]
2. Выполните команды по очереди:[cite: 1]
   - `netsh winsock reset`
   - `netsh int ip reset all`
   - `netsh winhttp reset proxy`
   - `ipconfig /flushdns`
3. Перезагрузите компьютер.[cite: 1]
</details>

<details>
<summary><b>Не работает веб-версия Telegram</b></summary>

Запустите **`service.bat`**, выберите **`Update hosts file`**, скопируйте текст из блокнота и добавьте его в системный файл `hosts` от имени администратора. Если не помогло — используйте [Desktop версию](https://github.com/telegramdesktop/tdesktop/releases) с [локальным прокси](https://github.com/calmaeromancerextol/tg-ws-proxy).[cite: 1]
</details>

<details>
<summary><b>Обход перестал работать / Не работают YouTube и Discord</b></summary>

- Стратегии могут со временем блокироваться. Пробуйте другие варианты (`ALT`/`FAKE`).[cite: 1]
- Убедитесь, что настроен **Secure DNS**.[cite: 1]
- Для Discord: выполните очистку кэша через `service.bat` -> `Run Diagnostics`, попробуйте браузерную версию `https://discord.com/app`.[cite: 1]
- Для YouTube: отключите блокировщик рекламы.[cite: 1]
</details>

<details>
<summary><b>Как полностью переустановить/обновить утилиту?</b></summary>

1. Сохраните свои файлы/данные.[cite: 1]
2. Перезагрузите устройство.[cite: 1]
3. Через `service.bat` выполните `Remove Services`.[cite: 1]
4. Удалите старую папку.[cite: 1]
5. Скачайте свежий релиз, разблокируйте архив и распакуйте в новую папку в корне диска без пробелов и кириллицы.[cite: 1]
6. Проверьте работу через `general` скрипты, после чего установите службу заново.[cite: 1]
</details>

<details>
<summary><b>Другие проблемы (игры, античит, Windows 7)</b></summary>

- **Игры:** обновите ipset через `service.bat` и включите `Game Filter` (`disabled`).[cite: 1]
- **Античит/WinDivert:** ознакомьтесь с инструкцией [windivert-hide](https://github.com/bol-van/zapret-win-bundle/tree/master/windivert-hide).[cite: 1]
- **Windows 7:** замените `WinDivert.dll` и `WinDivert64.sys` на файлы из папки [win7](https://github.com/bol-van/zapret-win-bundle/tree/master/win7).[cite: 1]
- Не нашли свою проблему? Создайте тикет в [Issues](https://github.com/calmaeromancerextol/zapret-discord-youtube/issues).[cite: 1]
</details>

---

## ⭐ Поддержка проекта

* Вы можете поддержать проект, поставив ⭐ этому репозиторию.[cite: 1]
* Материальная поддержка оригинального разработчика zapret доступна [тут](https://github.com/bol-van/zapret?tab=readme-ov-file#%D0%BF%D0%BE%D0%B4%D0%B4%D0%B5%D1%80%D0%B6%D0%B0%D1%82%D1%8C-%D1%80%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%87%D0%B8%D0%BA%D0%B0).[cite: 1]

## ⚖️ Лицензирование
Проект распространяется на условиях лицензии [MIT](https://github.com/calmaeromancerextol/zapret-discord-youtube/blob/main/LICENSE.txt).[cite: 1]

## 🩷 Благодарности
[![Contributors](https://contrib.rocks/image?repo=calmaeromancerextol/zapret-discord-youtube)](https://github.com/calmaeromancerextol/zapret-discord-youtube/graphs/contributors)[cite: 1]  
💖 Отдельная благодарность разработчику [zapret](https://github.com/bol-van/zapret) — [bol-van](https://github.com/bol-van).[cite: 1]