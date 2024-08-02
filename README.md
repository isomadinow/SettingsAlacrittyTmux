# Конфигурационные файлы для Alacritty и tmux

Этот репозиторий содержит конфигурационные файлы для терминала Alacritty и менеджера окон tmux. Следуя инструкциям ниже, вы сможете быстро настроить и использовать эти файлы.

## Содержание

- [Требования](#требования)
- [Установка](#установка)
- [Настройка Alacritty](#настройка-alacritty)
- [Настройка tmux](#настройка-tmux)

## Требования

Перед началом работы убедитесь, что у вас установлены следующие программы:

- [Alacritty](https://github.com/alacritty/alacritty)
- [tmux](https://github.com/tmux/tmux)

## Установка

1. Клонируйте репозиторий на ваш компьютер:

    ```sh
    git clone https://github.com/ваш_пользователь/configs.git
    cd configs
    ```

2. Скопируйте конфигурационные файлы в соответствующие директории:

    ```sh
    # Создаем директорию для конфигурационного файла Alacritty, если она не существует
    mkdir -p ~/.config/alacritty
    # Копируем конфигурационный файл Alacritty
    cp config/alacritty.toml ~/.config/alacritty/

    # Копируем конфигурационный файл tmux
    cp config/tmux.conf ~/.tmux.conf
    ```

## Настройка Alacritty

Файл конфигурации Alacritty находится по пути `~/.config/alacritty/alacritty.toml`. В этом файле вы можете настраивать различные параметры терминала, такие как шрифты, цвета, поведение курсора и т.д.

### Пример настройки Alacritty

- **Шрифт**: Настройка шрифта и его размера.

    ```toml
    font:
      normal:
        family: "Fira Code"
        style: "Regular"
      size: 12.0
    ```

- **Цветовая схема**: Изменение цветов фона, текста, курсора и выделения.

    ```toml
    colors:
      primary:
        background: '0x1e1e1e'
        foreground: '0xc5c8c6'
      cursor:
        text: '0x000000'
        cursor: '0xffffff'
    ```

- **Поведение окна**: Настройки по умолчанию для размеров окна, прозрачности и т.д.

    ```toml
    window:
      opacity: 0.9
      decorations: full
    ```

Для запуска Alacritty используйте команду:

```sh
alacritty

# tmux



## Установка

1. Клонируйте репозиторий на ваш компьютер:

    ```sh
    git clone https://github.com/ваш_пользователь/configs.git
    cd configs
    ```

2. Скопируйте конфигурационный файл в домашнюю директорию:

    ```sh
    cp config/tmux.conf ~/.tmux.conf
    ```

## Настройка tmux

Файл конфигурации tmux находится по пути `~/.tmux.conf`. В этом файле вы можете настраивать различные параметры и ключевые комбинации для управления окнами и панелями tmux.

### Пример настройки tmux

- **Ключевые комбинации**: Настройка горячих клавиш для управления окнами и панелями.

    ```sh
    # Устанавливаем префикс на Ctrl+a
    unbind C-b
    set-option -g prefix C-a
    bind-key C-a send-prefix
    ```

- **Статусная строка**: Изменение вида и содержания статусной строки.

    ```sh
    # Настройка статусной строки
    set -g status-bg colour235
    set -g status-fg colour136
    set -g status-left-length 40
    set -g status-right-length 90
    set -g status-interval 5
    ```

- **Поведение панелей**: Настройки для автоматического перезапуска программ в панелях, изменения размеров панелей и т.д.

    ```sh
    # Автоматический перезапуск панелей
    set -g remain-on-exit on
    ```

## Запуск tmux

Для запуска tmux используйте команду:

```sh
tmux source-file ~/.tmux.conf
  ```