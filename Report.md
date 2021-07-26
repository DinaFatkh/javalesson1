# Отчёт о тестировании Credit Card Number Validator

## Краткое описание

14.07.2021 было проведено ручное функциональное тестирование методом "белого ящика" приложения Credit Card Number Validator.

На тестирование затрачено: 1 час

В результате тестирования выявлены следующие дефекты:
* Баг-репорт №1 [Банковская карта с менее 16 цифрами в номере не проходит валидацию при вводе номера в файле Main.java](https://github.com/DinaFatkh/javalesson1/issues/1#issue-946721539)
* Баг-репорт №2 [Банковская карта с более 16 цифрами в номере не проходит валидацию при вводе номера в файле Main.java](https://github.com/DinaFatkh/javalesson1/issues/2#issue-946723667)

## Описание процесса тестирования

В процессе тестирования использовались следующие артефакты:
* [Тестовый набор проверки валидности банковской карты](https://github.com/DinaFatkh/javalesson1/blob/master/Testset.md)

В качестве тестовых данных использовались данные:

* сайт [kobzarev.com](https://www.kobzarev.com/other/testoviye-nomera-kreditnyh-kart/);
* сайт [freeformatter.com](https://www.freeformatter.com/credit-card-number-generator-validator.html);
* сайт [getcreditcardnumbers.com](https://www.getcreditcardnumbers.com/generated-credit-card-numbers).
  
Банковские карты разных платежных систем:

* 4716657376172601 Visa
* 4575043288813238 Visa
* 4929537796546848202 Visa
* 4222222222222 Visa
* 6011233269370590 Discover
* 6011991850461090 Discover
* 6011214349216146856 Discover
* 6011000990139424 Discover
* 5179022600029126 Master Card
* 2720990215278877 Master Card
* 5203898077600816 Master Card
* 5105105105105100 Master Card
* 6304930734815408 Maestro
* 6762127409787963 Maestro
* 6304507979549387 Maestro
* 586824160825533338 Maestro
* 370279509116218 American Express (AMEX)
* 340949327318355 American Express (AMEX)
* 378783221802536 American Express (AMEX)
* 371449635398431 American Express (AMEX)
* 3529407583317345 JCB
* 210081652918158 JCB
* 3534060751257481044 JCB
* 3566002020360505 JCB 

Тестирование производилось в следующем окружении:
* Windows 10 Pro, процессор x64
* Java 11

## Итоги тестирования

При реализации функциональности валидации номера банковской карты в приложении возникает проблема при вводе карт с меньшим или большим количеством цифр, чем 16, таким образом некторые платженые системы полностью или частично не проходят валидацию (пример, American Express (AMEX) или VISA). По итогу тестирования были заведены баг-репорты под каждую ситуацию с примерами карт.