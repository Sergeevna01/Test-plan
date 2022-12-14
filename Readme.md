# **План автоматизации тестирования возможности записи на обучение профессии ["Тестировщик ПО"](https://netology.ru/programs/qa) на сайте [Netology.ru](https://netology.ru/)**

**Виды применяемого тестирования** : тестирование методом черного ящика, тестирование удобства пользования, модульное тестирование.

**Валидными значениями для формы являются** : 

**-** обязательное поле "Имя": латиница, кириллица, пробел и дефис/тире, заполненный минимум двумя буквами.

**-** обязательное поле "Телефон": цифры, круглые скобки, пробел и дефис/тире в формате +9 (999) 999-99-99, от 9 до 14 символов включительно.



### **1. Перечень автоматизируемых сценариев:**

**Способы поиска формы для записи на курс обучения:**

**Вариант №1.**
На главной страницы сайта [Netology.ru](https://netology.ru/), с помощью выпадающего меню "**Каталог курсов**" - **Программирование** - **Тестировщик ПО;**

**Вариант №2.**
На главной страницы сайта [Netology.ru](https://netology.ru/), с помощью выпадающего меню "**Каталог курсов**" - **Полный каталог** - **Тестировщик ПО;**

**Вариант №3.**
На главной страницы сайта [Netology.ru](https://netology.ru/), с помощью картинки с надписью "**НЕО для начинающих**" - **Тестировщик ПО;**

**Вариант №4.**
На главной страницы сайта [Netology.ru](https://netology.ru/), с помощью раздела "**Актуальные темы**" - **Программирование** - **Тестировщик ПО;**

**Вариант №5.**
На главной страницы сайта [Netology.ru](https://netology.ru/), после раздела "**Раскройте свои сильные стороны**", с помощью кнопки "**Выбрать курс**" - **Тестировщик ПО;**

**Вариант №6.** На странице ["Тестировщик ПО"](https://netology.ru/programs/qa) - нажать на кнопку "Записаться";

**Вариант №7.** На странице ["Тестировщик ПО"](https://netology.ru/programs/qa) - прокрутить страницу до формы для записи на курс;

**Сценарии тестирования:**

1. Успешная отправка валидно заполненной [формы записи](https://netology.ru/programs/qa#/order) на курс "Тестировщик ПО", включая проверку ввода действующего промокода (с изменением стоимости курса) и перехода на страницы с условиями [политики](https://netology.ru/legal/11)  и  [пользовательского соглашения](https://netology.ru/legal/6)
2. Появление сообщения "Должно состоять из букв" у поля "Имя" при заполнение его спецсимволами в [форме записи](https://netology.ru/programs/qa#/order) на курс "Тестировщик ПО"
3. Появление сообщения "Должно состоять из букв" у поля "Имя" при заполнение его цифрами в [форме записи](https://netology.ru/programs/qa#/order) на курс "Тестировщик ПО"
4. Появление сообщения "Должно быть не короче 2 символов" у поля "Имя" при заполнение его одной буквой в [форме записи](https://netology.ru/programs/qa#/order) на курс "Тестировщик ПО"
5. Появление сообщения "Обязательное поле" у поля "Имя" при оставлении поля пустым в [форме записи](https://netology.ru/programs/qa#/order) на курс "Тестировщик ПО"
6. Появление сообщения "Номер в формате +9 (999) 999-99-99" у поля "Телефон" при заполнение поля 8 цифрами в [форме записи](https://netology.ru/programs/qa#/order) на курс "Тестировщик ПО"
7. Появление сообщения "Номер в формате +9 (999) 999-99-99" у поля "Телефон" при заполнение поля 15 цифрами в [форме записи](https://netology.ru/programs/qa#/order) на курс "Тестировщик ПО"
8. Появление сообщения "Обязательное поле" у поля "Телефон" при оставление поля пустым в [форме записи](https://netology.ru/programs/qa#/order) на курс "Тестировщик ПО"
9. Проверка статуса 200 и совпадения валидных данных отправленных [формы записи](https://netology.ru/programs/qa#/order) на курс "Тестировщик ПО" с данными в body POST-запроса к серверу и новыми данными из БД. 
10. Проверка статуса 500 и отсутствие новых записей в БД при отправке невалидного body в POST-запросе отправки [формы записи](https://netology.ru/programs/qa#/order) на курс "Тестировщик ПО"


### **2. Перечень используемых инструментов с обоснованием выбора**

**1. IntelliJ IDEA Community Edition** - интеллектуальная среда разработки. Умная и удобная среда разработки для Java с поддержкой всех последних технологий и фреймворков;

**2. Java JDK 11** - строго типизированный язык, синтаксис гораздо более читабельный, чем синтаксис C, C++;

**3. Gradle** - система автоматической сборки, построенная на принципах Apache Ant и Apache Maven, но предоставляющая DSL на языках Groovy и Kotlin вместо традиционной XML-образной формы представления конфигурации проекта.

**4. Faker** - библиотека для генерации случайных тестовых данных.

**5. JUnit 5** - тестовый фреймворк. Библиотека для модульного тестирования программного обеспечения на языке Java.

**6. Selenide** - это библиотека для написания лаконичных и стабильных UI тестов с открытым исходным кодом.

**7. Allure Framework** - популярный инструмент построения отчётов, упрощающий их анализ.

### **Перечень необходимых разрешений/данных/доступов**

1. Необходимо разрешение на тестирование возможности записи на обучение профессии ["Тестировщик ПО"](https://netology.ru/programs/qa) на сайте [Netology.ru](https://netology.ru/) 
2. Доступ к Базе Данных.

### **Перечень и описание возможных рисков при автоматизации**
1. Возможность изменения названия обучаемой профессии.
2. Возможность изменения структуры сайта.
3. Возможность изменения CSS-селекторов сайта.
4. Возможность изменения количество обязательных полей ввода данных, как для авторизованных, так и для неавторизованных пользователей сайта.
5. Возможность удаления обучаемой профессии.
6. Засорение БД ненужными записями.
7. Ложные запросы к менеджерам на обратный звонок.

### **Перечень необходимых специалистов для автоматизации**
Инженер (junior) по автоматизированному тестированию;

### **Интервальная оценка с учётом рисков (в часах);**
Для написания тестов и тестирования, подготовки отчетности необходимо **от 24 до 36 часов рабочего времени**.
