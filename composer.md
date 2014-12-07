Composer
========

Популярный менеджер зависимостей для PHP, ставший неотъемлемым инструментом для управления зависимостями в любом проекте.


## Установка

### Локально

Используя `curl`:
```bash
curl -sS https://getcomposer.org/installer | php
```

Используя сам PHP:
```bash
php -r "readfile('https://getcomposer.org/installer');" | php
```

### Глобально

```bash
curl -sS https://getcomposer.org/installer | php
mv composer.phar /usr/local/bin/composer
```

### Homebrew (для пользователей OSX)

```bash
brew update
brew tap homebrew/dupes
brew tap homebrew/php
brew install composer
```


## Старт нового проекта с Composer

Для начала перейдите в директорию с вашими проектом и запустите команду:

```bash
composer init
```
Вы можете четко указать версию, требуемую для запуска текущего проекта.
Для примера давайте укажем, что наш проект требует версию PHP 5.4 или свежее:

```bash
composer require PHP:~5.4
```


## Подключение библиотек


## Создание инструкций по автозагрузке файлов

Composer поддерживает генерацию пользовательских загрузчиков, соответствующих стандартам `psr-0`, `psr-2`, `psr-4`.

Это можно указать в `composer.json`:

```json
{
    "autoload": {
        "psr-4": {
            "MyNamespace\\": "src//myfolder",
            "AnotherLib\\SimpleNS": "src//anotherlib"
        }
    }
}
```
