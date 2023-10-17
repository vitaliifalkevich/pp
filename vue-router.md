# Тема заняття: Vue Router

## План заняття: 
1. Ознайомлення з офіційною бібліотекою маршрутизації vue-router (https://github.com/vuejs/vue-router, https://ru.vuejs.org/v2/guide/routing.html)
2. Встановлення бібліотеки vue-router та створення сторінки home, login, signup.
3. Створення захищених роутів (сторінка home має бути доступна тільки авторизованому користувачу, або вести на редірект на сторінку login для гостя)
4. Передача параметрів на сторінку через маршрутизацію.

## Хід роботи:

1. Ознайомлення з документацією vue-router, встановлення прикладу згідно з описом https://github.com/chrisvfritz/vue-2.0-simple-routing-example
> [!NOTE]
> **Встановлення залежностей**
> 
> ```npm install```
> 
> **Запуск проєкту за адресою http://localhost:8080 з авто перезавантаженням при змінах у коді (hot reload)**
> 
> ```npm run dev```

2. Створення сторінок Home, Login, Signup.

> [!NOTE]
> - Необхідно змінити стандартне оформлення прикладу маршрутизації
> - Кожна нова сторінка повинна бути виокремена у директорії pages.
> - У директорії templates повинно бути два шаблони (один для авторизованого користувача, інший - для гостя (для гостя - шаблон для сторінки реєстрації та логіну))
> - Елементи інтерфейсу, що повторюються необхідно розмістити у директорії components (кнопки, гіперпосилання тощо).
> - Сторінка логіну має містити гіперпосилання на сторінку реєстрації, сторінка реєстрації має містити посилання на сторінку логіну.
> - Сторінка реєстрації та логіну має один загальний шаблон, що розташовано у директорії /templates проєкту.
> - Валідація Email, пароля.
>  - Приклад регулярного виразу для валідації Email: <br/>
> ```/^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/``` <br/>
>  - Валідація пароля: від 8 символів, мін. одна цифра, мін. одна заглавна буква.
> - Верстка сторінок має бути зручна у використанні та логічна для розуміння користувачем, необхідне базове оформлення. Для тренування можна розглянути бібліотеки з UI компонентами для Vue та вправадити одну з обраних. Свій вибр пояснити.
> > Посилання: https://athemes.com/collections/vue-ui-component-libraries/
3. Створення захищених роутів та механізму аутентифікації
> [!NOTE]
> - Встановити та запустити приклад авторизації-аутентифікації за посиланням нижче:
> >Посилання: https://github.com/ratracegrad/Vue-Firebase-Auth-Tutorial
> 
> > Інструкція з встановлення: https://www.freecodecamp.org/news/how-to-add-authentication-to-a-vue-app-using-firebase/
> 
> - Необхідно зареєструватися у Firebase та згідно інструкції вище замінити доступи Firebase на свої
> ```
> var firebaseConfig = {
>   apiKey: "YourConfigHere",
>   authDomain: "YourConfigHere",
>   projectId: "YourConfigHere",
>   storageBucket: "YourConfigHere",
>   messagingSenderId: "YourConfigHere",
>   appId: "YourConfigHere"
> };
> ```
> - Перенести сторінки та компоненти, розроблені у другому пункті роботи у робочий приклад авторизації.
> - Якщо зайти на сторінку http://localhost:8080/dashboard після логіну з повним перезавантаженням сторінки - відбудеться редірект на головну.
> Необхідно внести правки, щоб при перезавантаженні сторінки після успішного логіну не відбувався редірект на головну сторінку.

4. Передача параметрів на сторінку через маршрутизацію.
> [!NOTE]
> - Створити сторінку /hobbies/:hobby, де :hobby - динамічний параметр.
> - Створити json файл за прикладом:
> ```
> {
>   "book": {
>     "name":"Книга"
>   },
>   "cinema": {
>     "name":"Кіно"
>   },
>   "dancing": {
>     "name":"Танці"
>   } 
> }
> ```
> - При введенні у url http://localhost:8080/hobbies/book має бути виведено на сторінці 
> "Моє хоббі: Книга". 
> 
> Інформація береться з JSON файлу. Якщо елемент не знайдено у JSON - виводиться текст "Не знайдено(:"

5. Завантажити у репозиторій код виконаної роботи та надати посилання на github (bitbucket, або gitlab).

 ## Контрольні запитання:
- Що таке та для чого потрібен Vue Router, які є аналоги?
- Які існують UI бібліотеки для Vue та для чого вони потрібні?
- Як реалізується механізм авторизації/аутентифікації?
- Як створювати та працювати з динамічними маршрутами?

## Корисні посилання:
- https://github.com/vuejs/vue-router
- https://ru.vuejs.org/v2/guide/routing.html
- https://router.vuejs.org/guide/advanced/navigation-guards.html
- https://router.vuejs.org/guide/essentials/nested-routes.html
- https://router.vuejs.org/guide/essentials/navigation.html
- https://router.vuejs.org/guide/essentials/route-matching-syntax.html
- https://router.vuejs.org/guide/essentials/named-routes.html
- https://router.vuejs.org/guide/essentials/named-views.html
- https://router.vuejs.org/guide/essentials/redirect-and-alias.html
- https://router.vuejs.org/guide/essentials/passing-props.html
- https://www.freecodecamp.org/news/how-to-add-authentication-to-a-vue-app-using-firebase/
