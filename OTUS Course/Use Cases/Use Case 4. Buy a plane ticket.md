
## Use Case 4. Купить авиабилет
|Цель|Купить билет на самолет|
| ------ | ------ |
|Где используется (система)	|Сервис покупки авиабилетов www.aviasales.ru|
|Предусловие|	Зарегистрированный пользователь авторизован в интернет магазине, корзина пользователя пуста, наличие товара на сайте интернет-магазина, наличие суммы на карте для оплаты товара|
|Успешное окончание	|Пользователь заказал выбранный товар, пришел e-mail об успешном заказе товара, оплата прошла успешно, списалась верная сумма, статус заказа отображается в ЛК|
|Неуспешное окончание|	Заказ не создан, не приходит e-mail об успешном заказе товара, не проходит оплата, списалась неверная сумма, статус заказа не отображается в ЛК|
|Актор|	Авторизованный пользователь|
|Триггер|	Авторизованному пользователю потребовалось купить товар|
|Переход к юзкейсу|	С карточки товара|
|Описание (шаги)|	Действие|
|1|	Актор добавляет товар в корзину|
|2|	Актор переходит в корзину и заполняет данные для доставки|
|3|	Актор выбирает способ доставки курьером|
|4|	Актор выбирает способ оплаты картой на сайте|
|5|	Актор оплачивает заказ|
|6|	Система оповещает об успешной оплате, отправляет на почту письмо с подтверждением заказа, отображает статус заказа в ЛК|
|Альтернативный сценарий	|
|2a	|Актор переходит в корзину и выбирает пункт самовывоза|
|3a	|Актор выбирает способ доставки самовывоз|
|4a	|Актор выбирает способ оплаты наличными курьеру|
|4b	|Актор выбирает способ оплаты картой курьеру|
|4c|	Актор выбирает способ оплаты сертификатом|
|Исключения	|
|5exc|	Недостаточно средств на карте|
|4с_exc|	Сертификат просрочен|
|6exc|	Актор не указал почту в ЛК|
