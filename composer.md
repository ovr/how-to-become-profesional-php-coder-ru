Composer
========

Популярный менеджер зависимостей для PHP, ставший неотъемлемым средством для урпавления зависимостями во всех проектах.

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

## Старт нового проект с Composer

Для начала перейдите в директорию с вашими проектом и запустите команду 

```bash
composer init
```

Вы можете четко устновить версию требуемую для запуска текущего проекта
Для примера давайте укажем что наш проект требует версию PHP 5.4 и более свежею

```bash
composer require PHP:~5.4
```

## Подключения библиотек

## Создания инструкций по автозагрузке файлов

Composer поддерживает генерацию пользовательских загрузчиков для стандартов `psr-0`, `psr-2`, `psr-4` 

Вы можете указать это в `composer.json`:

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
