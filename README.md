# 1. Перечень автоматизируемых сценариев
 *Сценарии навигации* <br>
 *Сценарии заполнения и отправки формы*
# 2.Перечень используемых инструментов с обоснованием выбора.
  1) Java версии 11 (jdk 11), IntelliJ Idea ver. 2023.3.4 (Community Edition)
  2) Подключенные зависимости:
     - Selenide (для поиска элементов на странице)
     - Faker (для генерации данных)
     - Allure (для просмотра отчетов о тестировании)
# 3.Перечень необходимых разрешений, данных и доступов.
  Прежде всего, необходимо запросить разрешение на проведение автоматизированного тестирования. После этого можно запросить доступ к API, к базе данных зарегистрированных пользователей.
# 4.Перечень и описание возможных рисков при автоматизации.
  1) Кратное увеличение времени на проектирование и реализацию автотестов из-за сложной внутренней стуктуры сайта (например, отсутствие тестовых меток для элементов страницы, что приводит к необходимости поиска других методов обращения к элементам)
  2) Падение автотестов после очередного обновления внутренней структуры страницы.
# 5.Перечень необходимых специалистов для автоматизации.
  Для решения задачи необходим 1 (один) автотестировщик с опытом разработки автотестов на Java (Gradle) с использованием инструментов работы с Selenide. <br>
  Для лучшего визуального контроля прохождения тестов рекомендуется подключить систему репортинга Allure.
# 6.Интервальная оценка с учётом рисков в часах.
  Примерные временные затраты на автоматизацию тестирования формы записи на курс "Тестировщик" - 7 часов.
