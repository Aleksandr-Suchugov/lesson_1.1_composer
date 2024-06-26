Скриншот созданного файла composer.json:
![alt text](https://github.com/Aleksandr-Suchugov/lesson_1.1_composer/blob/main/src/screenshot.JPG)


**В чем разница между файлами composer.json и composer.lock ?**

composer.json - содержит описание основных пакетов, включая требования к их версиям. 
composer.lock - содержит реальные версии пакетов, которые им были установлены на компьютер пользователя. Основное назначение файла состоит в полном сохранении среды, в которой осуществлялась разработка и тестирование проекта.

**В чем разница между директивами require-dev и require внутри файла composer.json?**

Для разработки и тестирования кода часто требуется более широкий список зависимостей, чем для запуска отладенного кода приложения в продакшн. Соответсвенно команда require-dev устанавливает зависимости необходимые для разработки и тестирования кода, а команда require - продакшн зависимости, для запуска и работы приложения/программы.

**В чем разница между запуском команды composer install и composer update?**

Команда composer install устанавливает те версии зависимостей, которые перечислены в composer.lock . В основном используется на стадии доставки кода в продакшн.
Команда composer update прочитает содержимое composer.json, удалит неактуальные более зависимости, проверит доступность последних версий зависимостей, установит последние версии зависимостей и обновит файл composer.lock . Часто используется в фазе разработки.