## Bordit - Java Hipster + blueprint Vue.js

## Описание:

Первый опыт работы с Java Hipster. Основной каркас пиложения полностью создан фраемворком JHipster. Каркас создан со следующими параметрами: 
* тип приложения - Монолит,
* БД - H2(PSQL), 
* сборщик Java - Maven,
* фронт - Vue.

### Задача:

Основная задача - создать WEB приложение, которое выполняет следующие функции:
- Ведение реестра клиентов с параметрами ФИО, возраст, телефон, e-mail, фото;
- Формирование справочника категорий;
- Ведение реестра товаров с параметрами название, цена, фото, категории (может быть указано несколько);
- Учет истории заказов с параметрами дата, клиент, набор товаров с указанием их количества.

С помощью https://start.jhipster.tech/jdl-studio/ был создан json файл для автоматического формирования сущностей в приложени - https://github.com/Tiunchik/jhip_bordit/blob/master/jdl.jh

### Доработки:

В дальнейшм приложение было доработано в ручном режиме:
* Удалён отдельный список позиция заказа;
* Списки позиций заказа добавлены каждый к своему Заказу; 
* Добавление позиций заказа перенесено в Заказ; 
* Реализована автоматическая привязка к Заказу при добавлении Эпозиции заказа. 
* Немного доработан функционал сервера - добавлена функция поиска позиций заказа по номеру заказа; 
* Добавлена проверка - при создании позиции заказа проходит сверка, исключающая добавление дублирующих позиций товара в одном заказе.

