# Отчёт о тестировании Credit Card Number Validator

## Краткое описание

14.07.2021 было проведено ручное функциональное тестирование методом "белого ящика" приложения Credit Card Number Validator.

На тестирование затрачено: 1 час

В результате тестирования выявлены следующие дефекты:
* Баг-репорт https://github.com/DinaFatkh/javalesson1/issues/1#issue-946721539
* Баг-репорт https://github.com/DinaFatkh/javalesson1/issues/2#issue-946723667

## Описание процесса тестирования

В процессе тестирования использовались следующие артефакты*:
* Баг-репорт

В качестве тестовых данных использовались данные с сайта https://www.kobzarev.com/other/testoviye-nomera-kreditnyh-kart/:

Банковские карты с 16 цифрами в номере:

* 4111111111111111 Visa - Result is OK
* 4012888888881881 Visa - Result is OK
* 4300000000000777 Visa - Result is OK
* 5000000000000009 Visa - Result is OK
* 4652060573334999 Visa - Result is OK
* 4000000000000119 Visa - Result is OK
* 6011111111111117 Discover - Result is OK
* 6011000990139424 Discover - Result is OK
* 3530111333300000 JCB - Result is OK
* 3566002020360505 JCB - Result is OK
* 5105105105105100 Master Card - Result is OK
* 5555555555554444 Master Card - Result is OK
* 6331101999990016 Switch/Solo (Paymentech) - Result is OK
* 5019717010103742 Dankort (PBS) - Result is OK
* 5610591081018250 Australian BankCard - Result is OK

Банковские карты с менее 16 цифрами в номере:

* 4222222222222 Visa - Result is FAIL
* 38520000023237 Dinners Club - Result is FAIL
* 30569309025904 Dinners Club - Result is FAIL
* 76009244561 Dankort (PBS)- Result is FAIL
* 378282246310005 American Express - Result is FAIL
* 371449635398431 American Express - Result is FAIL
* 378734493671000 Amex Corporate - Result is FAIL

Банковские карты с более 16 цифрами в номере:

* 586824160825533338 Maestro - Result is FAIL

Тестирование производилось в следующем окружении:
* Windows 10 Pro, процессор x64
* Java 11