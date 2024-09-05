## План тестирования

# 1. Перечень автоматизируемых сценариев.

Варианты навигации до страницы курса "Инженер по тестированию" с главной страницы:

 - вариант authorizationThroughProg

   1. Открыть сайт https://netology.ru/.
   2. Выбрать Направления обучения - Программирование.
   3. Ввести в строку поиска "Инженер по тестированию".
   4. Открывается страница курса. Нажать на кнопку "Записаться".
   5. Переход на форму со стоимостью курса и формой записи.
   6. Заполнить форму: "Имя","Телефон","Электронная почта".
   7. Нажать кнопку "Записаться".



- вариант authorizationThroughCatalog

  1. Открыть сайт https://netology.ru/.
  2. Нажать кнопку Каталог курсов. Открывается форма поиска. 
  3. Ввести в строке поиска "Инженер по тестированию".
  4. Нажать на название курса.
  5. Открывается страница курса. Нажать на кнопку "Записаться".
  6. Переход на форму со стоимостью курса и формой записи.
  7. Заполнить форму: "Имя","Телефон","Электронная почта".
  8. Нажать кнопку "Записаться".







Сценарии тестов с валидными данными:
1. Открыть сайт https://netology.ru/
2. Выбрать Направления обучения - Программирование
3. Ввести в строку поиска "Инженер по тестированию". Нажать на необходимый курс
4. На странице курса нажать на кнопку "Записаться"
5. Заполнить форму: "Имя", "Телефон", "Электронная почта"
 Описание валидных данных:
имя
     - на кириллице, например, "Иван";
     - на кириллице с дефисом, например, "Иван-Федор";
     - на кириллице двойное, например, Иван Федор;
     - на кириллице, с буквой Ё, например, "Семён";
телефон - 11 арабских цифр, например "+79532425113",
электронная почта на латинице с существующим доменом - "ivanivan@gmail.com".
7. Нажать кнопку "Записаться".
8. Ожидаемый результат: Всплывает сообщение: "Ваша заявка принята успешно. С вами свяжется наш менеджер".

Сценарии тестов с невалидными данными:
1. Ввод в форму имени на латинице
Ожидаемый результат: Поле "Имя" подсвечивается желтым.
2. Ввод в форму имени спецсимволов
Описание невалидных данных: имя из спецсимволов, кроме дефиса - "№;%:?*();
Ожидаемый результат: Под полем имени появляется надпись "Должно состоять из букв".
3. Ввод в форму имени цифр
Ожидаемый результат: Под полем имени появляется надпись "Должно состоять из букв".
4. Ввод в форму телефона из 10 цифр shouldNotAuthWithTenNumberPhone
Описание невалидных данных: телефон из 10 цифр - +7983267925;
Ожидаемый результат: При нажатии кнопки "Записаться" всплывает сообщение: "Номер телефона должен состоять из 11 цифр".
6. Ввод в форму телефона из 12 цифр
Описание невалидных данных: телефон из 12 цифр - +798326792534;
Ожидаемый результат: При нажатии кнопки "Записаться" всплывает сообщение: "Номер телефона должен состоять из 11 цифр".
7. Ввод в форму пустого поля имени/телефона/email
Ожидаемый результат: При заполнении формы под полем имени/телефона/email появляется красная надпись "Обязательное поле".
8. Ввод в форму электронной почты на кириллице
Ожидаемый результат: При введение в поле под полем появляется красная надпись "Неверный email".
9. Ввод в форму электронной почты с несуществующим доменом 
Ожидаемый результат: При введение в поле под полем появляется красная надпись "Неверный email".
10. Ввод в форму электронной почты из спецсимволов
Ожидаемый результат: При введение в поле под полем появляется красная надпись "Неверный email".


# 2. Перечень используемых инструментов с обоснованием выбора.

    2.1 JUnit 5, удобная среда тестирования для приложений Java.
    2.2 Selenide для автоматизированного тестирования WEB-приложений.
    2.3 Библиотека Faker, для рандомных данных.
    2.4 GitHub - хостинг IT-проектов.
    2.5 IT - это система контроля версий (VCS), которая позволяет отслеживать и фиксировать изменения в коде.
    2.3 Lombok, для удобства написания кода .
    2.6 Allure, для статистики по тестированию.
    2.7 Браузер Chrome, как наиболее популярный.

# 3. Перечень необходимых разрешений, данных и доступов.

   3.1 Разрешение на использование API.
   3.2 Доcтуп к БД.
   3.3 Вспомогательный класс с данными для тестов.

# 4. Перечень и описание возможных рисков при автоматизации.

   4.1 Изменение сайта
   4.2 Превышение срока выполнения задач
   4.3 Недостаточный уровень квалификации инженера

# 5. Перечень необходимых специалистов для автоматизации.

   Инженер по тестированию

# 6. Интервальная оценка с учётом рисков в часах.
   8 часов.
