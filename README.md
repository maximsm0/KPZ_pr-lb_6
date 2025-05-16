# Розробка UI для реалізації CRUD-операцій
# Мета
# Створити користувацький інтерфейс для взаємодії з реалізованим RESTful API, що надає можливість перегляду, створення, редагування та видалення екземплярів певної сутності. Розробка ведеться на базі React з використанням TanStack Router для реалізації маршрутизації. 
# Завдання
# Використовуючи boilerplate-проєкт vite-react-boilerplate, для сутності Post, яка була створена в роботі “Реалізація нової сутності, створення CRUD-операцій та відповідного RESTful API”, необхідно:
# 1. Сторінка колекції екземплярів сутності (/posts)
- Реалізувати рендеринг списку всіх доступних екземплярів сутності.
- Для кожного елемента відображати основну інформацію (ключові поля).
- Передбачити можливість переходу на сторінку конкретного екземпляра (/posts/:id).
- Додати кнопку "Створити новий екземпляр", яка веде на маршрут /posts/new.
- Реалізувати можливість видалення елемента з колекції (з підтвердженням дії)
# Реалізація:  
Реалізовано інтерфейс для роботи з сутністю "Post". На сторінці списку постів відображаються всі доступні записи з базовою інформацією, реалізована можливість видалення поста з підтвердженням дії. Кожен елемент має кнопку переходу до детальної сторінки, де показано повну інформацію про пост та доступне редагування. Також реалізовано окрему сторінку для створення нового поста. Для маршрутизації використовується TanStack Router. Вся логіка роботи з даними реалізована через mock-функції.  
- сторінка списку усіх постів PostListPage.tsx та css :  
![image](https://github.com/user-attachments/assets/ed25e254-5eaf-44c2-bb80-3a1c258543f5)  
![image](https://github.com/user-attachments/assets/d4680843-c696-4879-ad90-9d503234653b)  
- окремий PostItem.tsx (+css), який використовується в PostListPage.tsx:  
![image](https://github.com/user-attachments/assets/168a1df9-8692-4152-afa5-d1cf9489546e)
![image](https://github.com/user-attachments/assets/b5c614d0-c286-4211-ae92-7d740bd25806)  
![image](https://github.com/user-attachments/assets/4b757036-bc23-413c-99f4-28f4f4c37025)  
![image](https://github.com/user-attachments/assets/7b04ce59-f3fa-4fb9-af0b-eaca1e37355a)
- вікно для підтвердження видалення ConfirmModal.tsx:  
![image](https://github.com/user-attachments/assets/7f9fe68b-9f27-4f89-b802-e55639f9ce24)
![image](https://github.com/user-attachments/assets/41677859-cbea-434c-96b4-110ce35aedaa)
![image](https://github.com/user-attachments/assets/fc41f50c-3fbc-49b6-8c7e-12219f10fc17)  
- також використовуються mock-функції getAllEntities та deleteEntity:
![image](https://github.com/user-attachments/assets/e8b1e214-d855-44d7-98e2-71623f0503c7)
Сторінка колекції post: 
![image](https://github.com/user-attachments/assets/6a18bf6b-b454-4f3a-a198-c88f00b50910)
та підтвердження видалення:  
![image](https://github.com/user-attachments/assets/875489f3-12fc-40f0-b13d-3cc18a7a6f2d)
- Кнопка Create New Post перенаправляє на сторінку створення Post
- Кнопка Read More на окремому пості перенаправляє на сторінку Post
# 2.Сторінка окремого екземпляра сутності (/posts/:id або /posts/new)
## - У режимі перегляду (/posts/:id) реалізувати:
- відображення повної інформації про екземпляр;
- можливість редагування (форма з полями);
- кнопку для збереження змін (Update).
# Реалізація:  
- сторінка перегляду Post PostDetailPage.tsx + css:
![image](https://github.com/user-attachments/assets/01763c75-5f3e-4eac-a5e7-cb5220ca2d90)  
![image](https://github.com/user-attachments/assets/4136b937-e2c3-408b-933c-9e602f35c034)  
![image](https://github.com/user-attachments/assets/966456f1-fa76-4757-aeb5-21cb7249a193)  
![image](https://github.com/user-attachments/assets/5d26afa2-5965-44b5-b92a-fc3a9b89aa28)
- Також використовуються дві mock-функції getEntityById та updateEntity:
![image](https://github.com/user-attachments/assets/11a5437e-353c-4a47-bfe1-fbab90b6b4f6)

- Cторінка перегляду:
![image](https://github.com/user-attachments/assets/c1316da4-deb0-4fcc-8528-1bf974d9c158)
- Кнопка Back to Posts повертає назад на сторінку колекції Post
- Після натискання кнопки "Edit Post", відкривається форма:  
![image](https://github.com/user-attachments/assets/3b005e64-9b4f-4acb-91ea-e37e90e5f7e2)
- Кнопка Update зберігає зміни та перенаправляє назад на деталі Post
- Кнопка Cancel не зберігає ніякі зміни та перенаправляє назад на деталі Post
## - У режимі створення (/posts/new) реалізувати:
- форму з порожніми полями для введення нових даних;
- кнопку для збереження нового екземпляра (Create).
# Реалізація:  
- сторінка створення поста PostCreatePage.tsx + css
![image](https://github.com/user-attachments/assets/92e9ae5a-bb9b-4c5c-8157-3886502876cd)
![image](https://github.com/user-attachments/assets/697b7fe7-58b5-4915-b395-400502ef81b0)  
![image](https://github.com/user-attachments/assets/1b98d7f9-d94a-4584-a375-74d36e9815a9)  
![image](https://github.com/user-attachments/assets/513ae8bc-cebb-4863-af58-7037580fff1e)  
- Використовується mock-функція createEntity:  
![image](https://github.com/user-attachments/assets/e8921118-0b64-4c0a-ab7e-377219f20866)
- Сторінка Create:
![image](https://github.com/user-attachments/assets/382e7716-5730-4d98-b3d1-0377b87abc68)
- Спроба створити без заповнення полей:  
![image](https://github.com/user-attachments/assets/ddc03661-0768-4b96-a9d8-7ae3d3d0d6df)  
![image](https://github.com/user-attachments/assets/c508da43-bfc1-4fd8-a6f8-19003cc1a392)  
- Після створення переправляє на сторінку колекції постів
![image](https://github.com/user-attachments/assets/6a18bf6b-b454-4f3a-a198-c88f00b50910)  
- Для маршрутизації використовується TanStack Router:  
![image](https://github.com/user-attachments/assets/7eea34b6-091d-44a7-97c0-68a6b94cbadc)

# Висновок
На цій роботі я навчився розробляти інтерфейси для виконання CRUD-операцій, створювати зрозумілу структуру компонентів та забезпечувати їх взаємозв'язок. Я освоїв роботу з маршрутизатором TanStack Router для належної навігації між сторінками додатку, що зробило його більш динамічним і зручним у використанні. Також я поглибив свої знання у створенні форм для введення даних, валідації на клієнтській стороні та обробці помилок у процесі створення чи оновлення постів. Робота з mock-функціями дозволила мені зрозуміти принципи взаємодії з RESTful API для отримання, відправки, редагування та видалення даних. У результаті це був корисний практичний досвід, який допоміг мені зміцнити свої навички у розробці інтуїтивно зрозумілих і функціональних інтерфейсів.





