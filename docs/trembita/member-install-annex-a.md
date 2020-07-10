# Додаток А

## Інсталяція операційної системи Ubuntu Server 16.04.5 x64

Операційна система Ubuntu Server 16.04.5 LTS x64 використовується під час функціонування наступних компонентів Учасника СЕВДЕІР:

- шлюз безпечного обміну;
- сервер баз даних та архівування;
- сервер аналізу журналів подій.

Для створення віртуальної машини шлюзу безпечного обміну рекомендується використовувати наступні системи віртуалізації, які найбільш сумісні з захищеними носіями особистих ключів:

- VMware vSphere;
- Proxmox.

*Процес встановлення операційної системи на віртуальну машину*

Запустіть віртуальну машину з підключеним інсталяційним носієм операційної системи Ubuntu Server 16.04.5 x64 та виконайте послідно описані нижче дії.
Оберіть українську мову на першому кроці.

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-0]

Оберіть дію «Встановити Ubuntu Server».

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-1]

Підтвердіть встановлення українською мовою.

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-2]

Виберіть місце розташування «Україна».

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-3]

На питання «Визначити розкладку клавіатури?» оберіть варіант «Ні».

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-4]

У меню «Країна, для якої призначена дана клавіатура» - оберіть варіант «Ukrainian».

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-5]

Актуальна розкладка клавіатури: «Ukrainian».

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-6]

Оберіть зручний метод перемикання між національною та латинською розкладкою. Рекомендуємо обрати «Control+Shift», оскільки не завжди платформа віртуалізації коректно передає натиснення на деякі клавіши.

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-7]

На наступному кроці буде виконана спроба автоматичного налаштування мережевих параметрів за протоколом DHCP. Якщо у мережі, до якої підключений зазначений сервер (віртуальна машина) не має DHCP-сервера, вам потрібно налаштувати параметри мережі.

Далі задайте мережеве ім’я комп’ютера. Рекомендуємо його задати у відповідності з DNS-ім’ям вашого шлюзу безпечного обміну, якщо ви плануєте використовувати DNS-імена замість IP-адрес для вашого шлюзу.

На наступному кроці створіть користувача (введіть повне ім’я, якщо потрібно, або просто логін), який буде виконувати операції з адміністрування операційної системи при подальшому налаштуванні шлюзу безпечного обміну - адміністратор безпеки secadmin. 

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-8]

Тепер введіть логін (назву облікового запису) або залиште поле таким самим, як на попередньому кроці.

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-9]

Після цього необхідно встановити пароль для даного користувача. Рекомендації щодо пароля наведені на екрані.

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-10]

Пароль потрібно підтвердити.

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-11]

На питання щодо шифрування домашньої директорії потрібно відповісти «Ні».

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-12]

На наступному кроці система спробує визначити вашу часову зону. Перевірте, що вона відповідає дійсності, оскільки можуть виникнути проблеми внаслідок порушення синхронізації годинників.

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-13]

Рекомендуємо обрати варіант розбивки диску за замовчуванням - використати весь диск і налаштувати LVM.

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-14]

Обираємо диск.

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-15]

Підтверджуємо запис змін на диск.

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-16]

Підтверджуємо розмір розділу (використовуємо весь диск).

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-17]

Завершуємо розбивку та записуємо зміни на диск.

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-18]

Робота шлюзу безпечного обміну не передбачає використання проксі-серверів. Однак, на етапі встановлення можна його зазначити, якщо це необхідно для доступу до репозиторіїв з інсталяційними пакетами. Якщо проксі-сервера немає, залиште поле HTTP-проксі пустим.

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-19]

Після підтвердження інсталятор почне встановлювати базові компоненти операційної системи. Це може зайняти деякий час. Після завантаження базових компонентів оберіть варіант «Без автоматичних оновлень».

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-20]

Після цього на екрані «Вибір програмного забезпечення» встановіть позначку для консолі віддаленого адміністрування OpenSSH server за допомогою клавіши «пробіл».

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-21]

Встановлення завершується підтвердженням запису завантажувача GRUB.

![Встановлення OS][trembita-install-ubuntu-16-04-5-os-22]

Після цього необхідно вилучити інсталяційний носій та перезавантажити систему.

Наступним кроком з налаштування операційної системи є увімкнення інтерфейсу безпечного входу для користувачів.

Увійдіть в операційну системи з правами адміністратора безпеки та відкрийте на редагування наступний файл налаштувань:

```bash
sudo nano /etc/sysctl.d/10-magic-sysrq.conf
```

Замініть у цьому файлі значення параметру kernel.sysrq на 1:

<pre class="pre-file-1">
kernel.sysrq = 1
</pre>

Після цього збережіть зміни  та закрийте редактор за допомогою комбінації клавіш Ctrl+O, Enter, Ctrl+X. Перезавантажте операційну систему.

```bash
sudo shutdown -r now
```

Будь-який початок сеансу роботи з командною консоллю операційної системи необхідно починати за допомогою комбінації клавіш Alt + SysRq + K, з метою забезпечення безпечного інтерфейсу введення атрибутів адміністративного користувача.

Наступним кроком з інсталяції операційної системи є налаштування облікового запису системного адміністратора. Увійдіть в операційну системи користувачем з правами адміністратора безпеки та виконайти наступну команду:

```bash
sudo passwd root
```

Введіть двічі новий пароль системного адміністратора root.

> Примітка. Зверніть увагу, що при введенні паролю (password), символи, що ви вводите, не відображаються на екрані - це стандартне поводження операційної системи з паролями, що вводяться.

Останнім кроком є перевірка коректності встановленого системного часу. Перевірити поточний час можна за допомогою команди date. Встановити час можна за допомогою команди наступного формату:

```bash
sudo date --set "YYYY-MM-DD HH:MM:SS"
```

- YYYY - поточний рік у чотиризначному форматі,
- MM - поточний місяць у двозначному формати (починаючи з 01 до 12),
- DD - поточний день місяця, починаючи з 01,
- HH:MM:SS - поточна година.

[trembita-install-ubuntu-16-04-5-os-0]: /assets/images/trembita-install-ubuntu-16-04-5-os-0.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-1]: /assets/images/trembita-install-ubuntu-16-04-5-os-1.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-2]: /assets/images/trembita-install-ubuntu-16-04-5-os-2.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-3]: /assets/images/trembita-install-ubuntu-16-04-5-os-3.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-4]: /assets/images/trembita-install-ubuntu-16-04-5-os-4.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-5]: /assets/images/trembita-install-ubuntu-16-04-5-os-5.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-6]: /assets/images/trembita-install-ubuntu-16-04-5-os-6.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-7]: /assets/images/trembita-install-ubuntu-16-04-5-os-7.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-8]: /assets/images/trembita-install-ubuntu-16-04-5-os-8.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-9]: /assets/images/trembita-install-ubuntu-16-04-5-os-9.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-10]: /assets/images/trembita-install-ubuntu-16-04-5-os-10.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-11]: /assets/images/trembita-install-ubuntu-16-04-5-os-11.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-12]: /assets/images/trembita-install-ubuntu-16-04-5-os-12.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-13]: /assets/images/trembita-install-ubuntu-16-04-5-os-13.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-14]: /assets/images/trembita-install-ubuntu-16-04-5-os-14.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-15]: /assets/images/trembita-install-ubuntu-16-04-5-os-15.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-16]: /assets/images/trembita-install-ubuntu-16-04-5-os-16.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-17]: /assets/images/trembita-install-ubuntu-16-04-5-os-17.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-18]: /assets/images/trembita-install-ubuntu-16-04-5-os-18.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-19]: /assets/images/trembita-install-ubuntu-16-04-5-os-19.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-20]: /assets/images/trembita-install-ubuntu-16-04-5-os-20.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-21]: /assets/images/trembita-install-ubuntu-16-04-5-os-21.png  "Ubuntu Install"
[trembita-install-ubuntu-16-04-5-os-22]: /assets/images/trembita-install-ubuntu-16-04-5-os-22.png  "Ubuntu Install"