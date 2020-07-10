# Sophos

## Інсталяція антивірусного програмного забезпечення

Всі компоненти Учасника СЕВДЕІР повинні бути захищені антивірусним програмним забезпеченням.

Встановлення антивірусного ПЗ необхідно виконати на наступних компонентах промислового середовища СЕВДЕІР:

- робоча станція адміністратора;
- шлюз безпечного обміну;
- сервер баз даних та архівування;
- сервер аналізу журналів подій.

Наявність антивірусного ПЗ на тестових компонентах не є обов’язковою.

### Процес встановлення антивірусного програмного забезпечення

Завантажте антивірусне програмне забезпечення Sophos Antivirus for Linux версії 9 з наступного інтернет ресурсу - [https://www.sophos.com/en-us/products/free-tools/sophos-antivirus-for-linux.aspx](https://www.sophos.com/en-us/products/free-tools/sophos-antivirus-for-linux.aspx). В процесі завантаження вам необхідно зареєструватися на зазначеному порталі.

Завантажений інсталяційний пакет розархівуйте за допомогою наступної команди та перейдіть у директорію *sophos-av*:

```bash
tar -zxvf sav-linux-free-9.tgz
cd sophos-av/
```

Запустіть інсталяцію наступною командою:

```bash
sudo ./install.sh
```

![Встановлення Sophos][trembita-install-sophos-antivirus-0]

Після перегляду ліцензійної угоди [натисніть клавішу Enter для продовження] необхідно її прийняти. Натисніть клавішу Y, потім Enter.

![Встановлення Sophos][trembita-install-sophos-antivirus-1]

Оберіть тип оновлення з офіційного джерела постачальника антивірусного програмного забезпечення. Для цього введіть літеру s та натисніть клавішу Enter на запит «Which type of auto-updating do you want?».

![Встановлення Sophos][trembita-install-sophos-antivirus-2]

Оберіть тип ліцензії «Безкоштовна» (Free). Для цього на запитання «Do you wish to install the Free (f) or Supported (s) version of SAV for Linux?» введіть літеру f та натисніть Enter.

![Встановлення Sophos][trembita-install-sophos-antivirus-3]

Наступним кроком необхідно обрати режим доступу до серверів оновлень. Якщо ви не маєте проксі-сервера для доступу до мережі Інтернет, введіть літеру N та натисніть Enter.

У випадку, якщо ви використовуєте проксі-сервер, зверніться до інструкції користувача, доступної на офіційному сайті виробника антивірусного програмного забезпечення.

![Встановлення Sophos][trembita-install-sophos-antivirus-4]

![Встановлення Sophos][trembita-install-sophos-antivirus-5]

На цьому процес інсталяції антивірусного програмного забезпечення завершено.

[trembita-install-sophos-antivirus-0]: /assets/images/trembita-install-sophos-antivirus-0.png  "Sophos Antivirus"
[trembita-install-sophos-antivirus-1]: /assets/images/trembita-install-sophos-antivirus-1.png  "Sophos Antivirus"
[trembita-install-sophos-antivirus-2]: /assets/images/trembita-install-sophos-antivirus-2.png  "Sophos Antivirus"
[trembita-install-sophos-antivirus-3]: /assets/images/trembita-install-sophos-antivirus-3.png  "Sophos Antivirus"
[trembita-install-sophos-antivirus-4]: /assets/images/trembita-install-sophos-antivirus-4.png  "Sophos Antivirus"
[trembita-install-sophos-antivirus-5]: /assets/images/trembita-install-sophos-antivirus-5.png  "Sophos Antivirus"