## Проблемы
- Ошибки взаимодействия между этими сервисами, связанные с задержками ответов или ошибками при взаимодействии с API страховых компаний
- Данные могут устаревать или быть несогласованными между сервисами

## Риски
- Сбой всей цепочки из-за одной ошибки (ошибки на стороне одной страховой компании могут блокировать ответы ins-product-aggregator)
- Низкая масштабируемость архитектуры. Рост числа запросов от core-app и ins-comp-settlement увеличивает нагрузку на ins-product-aggregator
- Рост числа страховых компаний (с 5 до 10) увеличит время ожидания ответа и вероятность ошибок
- Зависимость сервисов друг от друга из-за использования синхронного метода взаимодействия