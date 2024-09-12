1
Створення Віртуальної Машини:

Запустив VirtualBox і створив нову віртуальну машину.
Налаштував основні параметри: назву, тип та версію операційної системи (Ubuntu), розмір оперативної пам'яті.
Створив новий віртуальний жорсткий диск у форматі VDI з динамічним виділенням обсягу (20 ГБ).
Налаштування Мережі:

Налаштував мережевий адаптер на тип Bridged Adapter, щоб VM отримувала IP-адресу з локальної мережі.
Інсталяція Операційної Системи:

Завантажив ISO-образ Ubuntu та додав його як оптичний диск у налаштування VM.
Запустив віртуальну машину і виконати інсталяцію Ubuntu.
Збереження та Відновлення Стану VM:

Створив знімок VM після початкового налаштування системи.
Перевірив функціональність відновлення знімка, відновивши VM до стану, зафіксованого у знімку.
Зміна Розміру Диска:

Збільшив розмір диска з 20 ГБ до 30 ГБ.
Розширив файлову систему в Ubuntu для використання нового простору.


2
Після початкового налаштування віртуальної машини і встановлення Ubuntu, я створив знімок системи. Це дозволило зберегти точний стан VM на момент завершення початкових налаштувань.

3
Після завершення тестування я вирішив відновити VM до початкового стану, щоб повернутися до чистого середовища.
Я вибрав знімок, створений раніше, і використав функцію Restore (Відновити) у VirtualBox.
Система автоматично відновила всі налаштування та файли, які були на момент створення знімка, видаливши всі зміни, внесені після цього.

4
Зміна Розміру Жорсткого Диска:

Відкрив налаштування VM і перейшов до вкладки Storage .
Вибрав жорсткий диск, який потрібно змінити, і натиснув на кнопку Resize .
Збільшив розмір диска з 20 ГБ до 30 ГБ.
Результат: Диск був розширений, але для використання нового простору потрібно було розширити файлову систему всередині операційної системи.
Налаштування Мережі:

Перейшов до вкладки Network .
Вибрав Bridged Adapter  для підключення VM до локальної мережі.
Це дозволило VM отримати IP-адресу з локальної мережі та забезпечило безпосередній доступ до інших пристроїв у мережі.
Додавання ISO-образу:

У налаштуваннях VM перейшов до вкладки Storage .
Додав ISO-образ Ubuntu як оптичний диск.
Результат: Можливість завантажити та інсталювати Ubuntu на віртуальну машину з використанням ISO-образу.
Відновлення до Початкового Стану:

У вкладці Snapshots  вибрав знімок, створений раніше.
Використав функцію Restore  для повернення VM до стану, зафіксованого у знімку.
Результат: Віртуальна машина повернулася до початкового стану з усіма налаштуваннями та файлами, які були на момент створення знімка, з усуненням всіх змін, внесених після цього.