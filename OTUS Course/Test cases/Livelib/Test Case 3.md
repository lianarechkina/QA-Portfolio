## [LIB-8983] Подписка на рассылку через настройки профиля пользователя

Приоритет Средний (Medium)
Серьезность Незначительный (Minor)

Предусловия
1. Пользователь авторизован на сайте [www.livelib.ru](https://www.livelib.ru/)
2. Валидные данные для входа  
логин: test01, пароль: Qwerty123
3. У профиля указана и подтверждена почта test01@gmail.com, пароль : Qwerty123
4. Открыта страница профиля пользователя

|№| Действия | Ожидаемый результат |
|---|----|----|
|1| Нажать кнопку "Настройки" | Открывается выпадающий список |
|2| Выбрать раздел "Настройки аккаунта и уведомлений" | Открывается страница "Настройки уведомлений" |
|3| Установить флаг "Получать рассылку" | Флаг установлен |
|4| Нажать кнопку "Сохранить" | 1. Страница обновилась   |
||  | 2. Появилось уведомление "Настройки обновлены" |
|5| Авторизоваться на почте Gmail | Отображается почта |
|6| Открыть письмо от "LiveLib" | Отображается сообщение |
|7| Подтвердить действие с подпиской на новости переходом по ссылке | 1. Отображается сайт "LiveLib" |
||  | 2. Подписка на новости подтверждена|
