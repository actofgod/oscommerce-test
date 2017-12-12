# yandex-money-cms-v2-oscommerce

С помощью модуля можно настроить прием платежей через Яндекс.Кассу

[Инструкция по настройке](https://kassa.yandex.ru/manuals/oscommerce)

Для установки данного модуля необходимо переместить папки `ext`, `includes` и файл `callback.php` из папки `src` [архива](https://github.com/yandex-money/yandex-money-cms-v2-oscommerce/archive/master.zip) в корень Вашего сайта.

По умолчанию модуль устанавливается для работы с Яндекс.Кассой, для того чтобы его изменить в файле [src/ext/modules/payment/yandex_money/yandex_money.php](src/ext/modules/payment/yandex_money/yandex_money.php) найдите строки:
```php
// Устанавливаем режим работы:
// MODULE_PAYMENT_YANDEXMONEY_MODE1 - Яндекс.Касса
// MODULE_PAYMENT_YANDEXMONEY_MODE2 - Яндекс.Деньги
// MODULE_PAYMENT_YANDEXMONEY_MODE3 - Яндекс.Платёжка
define('MODULE_PAYMENT_YANDEXMONEY_MODE', MODULE_PAYMENT_YANDEXMONEY_MODE1);
```
И замените объявление константы MODULE_PAYMENT_YANDEXMONEY_MODE:
* `define('MODULE_PAYMENT_YANDEXMONEY_MODE', MODULE_PAYMENT_YANDEXMONEY_MODE2);` для того чтобы подключить оплату через Яндекс.Деньги;
* `define('MODULE_PAYMENT_YANDEXMONEY_MODE', MODULE_PAYMENT_YANDEXMONEY_MODE3);` чтобы использовать Яндекс.Платёжку.

Далее рекомендуем следовать пунктам [инструкции](https://kassa.yandex.ru/manuals/oscommerce).

Пожалуйста, обязательно делайте бекапы!

### О Кассе
Сервис, который позволяет включить прием платежей на сайте.

[Сайт Кассы](http://kassa.yandex.ru/)

#### Условия
* подходит для юрлиц и ИП,
* деньги приходят на расчетный счет, 
* комиссия берется с каждого успешного платежа.

Для использования нужно [подключиться к Яндекс.Кассе](https://money.yandex.ru/joinups) и получить в личном кабинете на сайте Кассы параметры **shopId** и **Секретный ключ**.

### Способы приема платежей
Вы можете выбрать любое количество способов из списка:

* Банковские карты — Visa, Mastercard и Maestro, «Мир»;
* Яндекс.Деньги;
* Webmoney;
* QIWI Wallet;
* Наличные;
* Альфа-Клик;
* Сбербанк Онлайн;
* Баланс мобильного — Билайн, Мегафон, МТС, Tele2.

### Дополнительные возможности

**Оплата на стороне Яндекса**

Включите в модуле оплату на стороне Яндекса — и не придется размещать на своем сайте все способы оплаты. Вместо этого останется одна кнопка «Заплатить».
 
[Пример в демо-магазине Кассы](https://kassa.yandex.ru/demo/index.html)

**Отправка данных для чеков по 54-фз**

Если вы подключите решение Кассы для 54-фз, модуль будет отправлять в Кассу данные для чека вместе с информацией о заказе.
 
[Подробности на сайте Кассы](https://kassa.yandex.ru/features) 

### Контакты
Если у вас есть вопросы или идеи для модуля, напишите нам: cms@yamoney.ru

В письме укажите:
* версию платформы,
* версию модуля (его можно посмотреть на странице настроек),
* идею или проблему,
* снимок экрана, о котором говорите.
