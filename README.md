# План автоматизации тестирования записи на обучение профессии «Тестировщик ПО» 
## 1. Перечень автоматизируемых сценариев
### Сценарии навигации: <br>
   - #### *Сценарий поиска через кнопку "Каталог курсов" на главной странице сайта:*</u>
  1. Найти на главной странице сайта Netology.ru кнопку "Каталог курсов" (*тестовая метка: "data-testid=header-navigatorBtn"*)
  2. Кликнуть по кнопке "Каталог курсов"
  3. Кликнуть по ссылке "Программирование" (*SelenideElement "а href=development"*)
  4. Прокрутить страницу вниз до ссылки "Тестировщик ПО" (*SelenideElement "data-program-id=46882"*)
  5. Кликнуть по тексту "Тестировщик ПО" <br>
  6. Найти форму записи на курс с полями ввода имени, номера телефона и кнопкой "Получить консультацию" (*SelenideElement "id=presentation_order"*)
   - #### *Сценарий поиска через ссылку "Программирование" на главной странице сайта:*
  1. Найти на главной странице сайта Netology.ru ссылку "Программирование" (*SelenideElement "а href=development"*)
  2. Кликнуть по ссылке "Программирование" (*SelenideElement "а href=development"*)
  3. Прокрутить страницу вниз до ссылки "Тестировщик ПО" (*SelenideElement "data-program-id=46882"*)
  4. Кликнуть по тексту "Тестировщик ПО" <br>
  5. Найти форму записи на курс с полями ввода имени, номера телефона и кнопкой "Получить консультацию" (*SelenideElement "id=presentation_order"*)
  - #### *Сценарий поиска на главной странице сайта*
  1. Прокрутить главную страницу сайта вниз до формы "Вопросы" (*SelenideElement "id=questions"*)
  2. Найти форму записи на курс с полями ввода имени, номера телефона и кнопкой "Получить консультацию"
 ### Сценарии заполнения и отправки формы:<br>
  - #### *Заполнение формы ввода валидными данными с помощью Faker:*
    + Сгенерировать валидные данные имени пользователя с помощью Faker с локалью "ru".
    + Вставить сгенерированные данные в поле "Имя" (*SelenideElement "name=first_name"*)
    + Сгенерировать валидный номер телефона с помощью Faker.
    + Вставить сгенерированные номер телефона в поле "Телефон" (*SelenideElement "name=phone"*)
    + Нажать кнопку "Получить консультацию" (*SelenideElement "type=submit"*) <br><br>
    *Ожидаемый результат:* Появление всплывающего окна с текстом: "Ваша заявка принята!" <br>
 - #### *Нажатие кнопки "Получить консультацию" при вводе невалидных данных в поле "Имя"*
    + Сгенерировать невалидные данные имени пользователя(например, с помощью Faker с локалью "en").
    + Вставить сгенерированные данные в поле "Имя" (*SelenideElement "name=first_name"*)
    + Сгенерировать валидный номер телефона с помощью Faker.
    + Вставить сгенерированные номер телефона в поле "Телефон" (*SelenideElement "name=phone"*)
    + Нажать кнопку "Получить консультацию" (*SelenideElement "type=submit"*) <br><br>
    *Ожидаемый результат:* Появление всплывающего окна с текстом: "Проверьте правильность ввода имени" <br>
- #### *Нажатие кнопки "Получить консультацию" при вводе невалидных данных в поле "Телефон"*
    + Сгенерировать валидные данные имени пользователя с помощью Faker с локалью "ru".
    + Вставить сгенерированные данные в поле "Имя" (*SelenideElement "name=first_name"*)
    + Вставить невалидный номер телефона (например, состоящий из букв: "телефон") в поле "Телефон" (*SelenideElement "name=phone"*)
    + Нажать кнопку "Получить консультацию" (*SelenideElement "type=submit"*) <br><br>
    *Ожидаемый результат:* Появление всплывающего окна с текстом: "Проверьте правильность ввода номера телефона" <br>
## 2.Перечень используемых инструментов с обоснованием выбора.
  1) Java версии 11 (jdk 11), IntelliJ Idea ver. 2023.3.4 (Community Edition)
  2) Подключенные зависимости:
     - Selenide (для поиска элементов на странице)
     - Faker (для генерации данных)
     - Allure (для просмотра отчетов о тестировании)
## 3.Перечень необходимых разрешений, данных и доступов.
  Прежде всего, необходимо запросить разрешение на проведение автоматизированного тестирования. После этого можно запросить доступ к API, к базе данных зарегистрированных пользователей.
## 4.Перечень и описание возможных рисков при автоматизации.
  1) Кратное увеличение времени на проектирование и реализацию автотестов из-за сложной внутренней стуктуры сайта (например, отсутствие тестовых меток для элементов страницы, что приводит к необходимости поиска других методов обращения к элементам)
  2) Падение автотестов после очередного обновления внутренней структуры страницы и, например, изменения тестовых меток.
## 5.Перечень необходимых специалистов для автоматизации.
  Для решения задачи необходим 1 (один) автотестировщик с опытом разработки автотестов на Java (Gradle) с использованием инструментов работы с Selenide. <br>
  Для лучшего визуального контроля прохождения тестов рекомендуется подключить систему репортинга Allure.
## 6.Интервальная оценка с учётом рисков в часах.
  Примерные временные затраты на автоматизацию тестирования формы записи на курс "Тестировщик" - 7 часов.
