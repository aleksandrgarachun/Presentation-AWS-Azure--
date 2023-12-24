# Порівняння ефективності розподілених баз даних у хмарному середовищі: AWS та Azure
---
![AWS VS Azure](./photos/azure-vs-aws.jpg)

---
Хмарні технології стають неодмінною складовою інфраструктури для сучасних компаній, які прагнуть забезпечити ефективну роботу, масштабованість та доступність своїх інформаційних ресурсів. Ключовим аспектом цієї інфраструктури є розподілені бази даних, які грають критичну роль у забезпеченні швидкого та надійного доступу до даних у реальному часі.

В даному контексті два основних хмарних провайдера, Amazon Web Services (AWS) та Microsoft Azure, пропонують відмінні рішення для розподілених баз даних. У цьому порівняльному аналізі ми розглянемо дві ключові послуги цих платформ - AWS DynamoDB та Azure Cosmos DB, звертаючи увагу на їхні можливості, продуктивність, моделі даних, масштабованість та вартість. Розглядаючи ці аспекти, ми спробуємо визначити оптимальний вибір для різних сценаріїв використання та бізнес-потреб.

---

### AWS
Amazon Web Services (AWS) - це провідний світовий хмарний сервіс, який надає широкий спектр послуг для забезпечення інфраструктури, обробки даних, штучного інтелекту, машинного навчання, інтернету речей та багатьох інших сфер. 

### Ініціалізація клієнта для AWS DynamoDB:
![Ініціалізація клієнта для AWS DynamoDB](./photos/carbon1.png)


### Azure
Azure пропонує широкий вибір реляційних та нереляційних баз даних для забезпечення будь-яких потреб вашої програми. Вбудовані засоби штучного інтелекту дозволяють автоматизувати такі завдання управління, як високий рівень доступності, масштабування та налаштування продуктивності запитів, забезпечуючи безперервну роботу ваших додатків. Підтримуйте критично важливі програми з необмеженим масштабом баз даних та доступністю до 99,999%. Такі компоненти Azure, як вбудовані елементи управління безпекою даних, широке охоплення регіонів та провідні в індустрії сертифікації відповідності, дозволяють вам посилити безпеку та забезпечити зростання бізнесу.
### Ініціалізація клієнта для Azure Cosmos DB:
![Ініціалізація клієнта для AWS DynamoDB](./photos/carbon2.png)

--- 
### Порівняльний аналіз
| **Аспект**                         | **DynamoDB (AWS)**                                                | **Cosmos DB (Azure)**                                              |
| -----------------------------------| ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| **Моделі даних**    | Модель даних: Ключ-значення (NoSQL).                     | Моделі даних: Підтримка документів, ключ-значення, графів, колонок (мультімодальний підхід).
| **Мови Запитів**    | Мова запитів: AWS SDK підтримує операції CRUD та складні запити.                     | Мова запитів: SQL-подібна мова (SQL API), а також мови, специфічні для моделей даних.|
| **Масштабованість** | Масштабованість: Автоматичне масштабування з визначенням пропускної здатності.| Масштабованість: Глобальна реплікація з масштабуванням на основі моделі пропускної здатності або фіксованого об'єму даних. |
| **Продуктивність** | Продуктивність: Гарантує низьку затримку та високу доступність. | Продуктивність: Гарантована низька затримка завдяки мультирегіональній реплікації. |
| **Гарантії** | Гарантії: AWS гарантує низьку затримку та високу доступність з використанням регіональних центрів даних. | Гарантії: Гарантується масштабованість та доступність з урахуванням SLA. |
| **Спрощення Управлінням** | Управління: Завдяки керованому сервісу, AWS бере на себе багато завдань з управління базою даних. | Управління: Повністю керований сервіс, який включає автоматичне масштабування та резервне копіювання. |
| **Ціноутворення**       | Ціноутворення: Орієнтоване на використання пропускної здатності та сховища даних. | Ціноутворення: Враховує кількість прочитаних, записаних та видалених одиниць, а також використання пропускної здатності. |
| **Вартість**       | Безкоштовна лімітація: AWS пропонує безкоштовну кількість прочитаних та записаних одиниць пропускної здатності в межах обмежень регіону. | <br>Безкоштовна лімітація: Azure Cosmos DB пропонує обмежену кількість безкоштовних одиниць пропускної здатності та об'єму даних. |


---

### Приклади коду для створення базових ресурсів у кожному з сервісів:

> Приклад коду для AWS (використовуючи AWS SDK для Python - Boto3):
>> Створення Amazon S3 Bucket:
![Створення Amazon S3 Bucket](./photos/carbon3.png)
Створення Amazon EC2 Instance:
![Створення Amazon EC2 Instance](./photos/carbon4.png)

> Приклад коду для Azure (використовуючи Azure SDK для Python):
>> Створення Azure Storage Account::
![Створення Azure Storage Account:](./photos/carbon5.png)
Створення Azure Virtual Machine::
![Створення Azure Virtual Machine:](./photos/carbon6.png)

 Ці приклади демонструють базовий синтаксис для створення об'єктів у сервісах облікових записів та віртуальних машинах для AWS та Azure відповідно. Пам'ятайте, що код може бути значно складнішим в залежності від конкретних вимог та розгалуженості вашого проекту.

 ---

### Коли використовувати AWS та Azure?
AWS варто вибрати, коли проект потребує широкого спектру різноманітних сервісів. З гнучкістю та розгалуженістю свого екосистеми, AWS забезпечує велику кількість інструментів для будь-якого завдання. Але якщо ваша компанія вже використовує продукти Microsoft, Azure може бути більш логічним вибором, оскільки він легше інтегрується з існуючою інфраструктурою та допомагає уніфікувати робочий процес. Якщо ваш проект передбачає значний обсяг роботи та географічну розгалуженість, AWS, зі своєю величезною глобальною мережею дата-центрів, може бути найоптимальнішим вибором. Azure в свою чергу часто вважається оптимальним рішенням для великих підприємств, оскільки він пропонує широкі можливості управління та безпеки для великих обсягів даних та великих корпоративних систем.

При виборі між Amazon Web Services (AWS) та Microsoft Azure слід враховувати ряд ключових факторів, що визначатимуть оптимальність кожної платформи для конкретного проекту чи бізнес-завдання. Ці дві хмарні платформи є лідерами у своїй галузі, проте вони мають свої унікальні особливості, які можуть бути важливими залежно від конкретних потреб та стратегій вашої компанії!


__Виконав:__
_Гарачун Олександр ІМ-23_ [telegram: @aleksandrgarachun](https://t.me/aleksandrgarachun)