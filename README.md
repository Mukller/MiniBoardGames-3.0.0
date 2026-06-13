<div align="center">

[![License: MIT](https://img.shields.io/badge/License-MIT-purple?style=flat-square)](LICENSE.md)
[![maintained](https://img.shields.io/badge/maintained%3F-yes-green?style=flat-square)](https://github.com/Mukller/MiniBoardGames-3.0.0)
[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen?style=flat-square)](CONTRIBUTING.md)

</div>

<details open>
<summary><strong>📖 English</strong></summary>

# DailyStreak 3.0.0

🎮 **Minecraft Plugin** for adding mini-games directly to your server

## Description

DailyStreak is a powerful Minecraft server plugin that allows players to participate in a variety of mini-games. Perfect for entertaining your community!

## Features

- 🎮 20+ Mini-Games
- 👥 Full Multiplayer Support
- ⚙️ Flexible Configuration
- 💾 Statistics Tracking
- 🏆 Reward System

## Requirements

- Java 11 or higher
- Minecraft Server 1.16.5+
- Bukkit/Spigot/Paper

## Installation

1. Download DailyStreak.jar
2. Place in /plugins/ folder
3. Restart server
4. Configure in config.yml

## Commands

- `/ds help` - Plugin help
- `/ds play <game>` - Start a game
- `/ds list` - List games
- `/ds stats` - Your statistics

## License

MIT License - See LICENSE.md for details

## Author

Mukller - [@Mukller](https://github.com/Mukller)

Made with ❤️ by Mukller

</details>

<details>
<summary><strong>📖 Русский</strong></summary>

# MiniBoardGames 3.0.0

<div align="center">

🎮 **Minecraft Plugin** для добавления мини-игр прямо на ваш сервер

[![License: MIT](https://img.shields.io/badge/License-MIT-purple?style=flat-square)](LICENSE.md)
[![Minecraft](https://img.shields.io/badge/Minecraft-1.16%2B-green?style=flat-square)](https://minecraft.net)
[![Java](https://img.shields.io/badge/Java-11%2B-blue?style=flat-square&logo=java)](https://www.java.com/)
[![PaperMC](https://img.shields.io/badge/PaperMC-Latest-orange?style=flat-square)](https://papermc.io)
[![maintained](https://img.shields.io/badge/maintained%3F-yes-green?style=flat-square)](https://github.com/Mukller/MiniBoardGames-3.0.0)
[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen?style=flat-square)](CONTRIBUTING.md)

[English](README_EN.md) • Русский

</div>

---

## 📋 Описание

**MiniBoardGames** — это мощный и гибкий плагин для Minecraft серверов, позволяющий игрокам участвовать в разнообразных мини-играх прямо на сервере. Он идеален для создания увлекательного игрового опыта, развлечения сообщества и стимуляции взаимодействия между игроками.

Плагин поддерживает большое количество настраиваемых мини-игр, от классических карточных игр до современных аркад.

---

## ✨ Основные возможности

- 🎮 **20+ встроенных мини-игр** (2048, Флеппи Берд, Морской бой, Джек или Дама и многие другие)
- 👥 **Полная поддержка мультиплеера** (от 1 до N игроков в одной партии)
- ⚙️ **Гибкая система конфигурации** (каждая игра настраивается отдельно)
- 💾 **Сохранение статистики** (отслеживание побед, проигрышей и рейтинговых баллов)
- 🏆 **Встроенная система наград** (монеты, очки опыта, предметы)
- 🌍 **Поддержка локализации** (русский язык и легкость добавления других)
- 🔧 **Система горячей перезагрузки** (изменение конфигов без перезапуска сервера)
- 📊 **Детальная база данных** (сохранение всех игровых событий)

---

## 📋 Требования

| Компонент | Версия | Примечания |
|-----------|--------|-----------|
| **Java** | 11 или выше | Необходимо для запуска плагина |
| **Minecraft Server** | 1.16.5+ | Поддержка всех версий начиная с 1.16.5 |
| **Bukkit/Spigot/Paper** | Любой modern fork | Полная совместимость |

---

## 🚀 Установка

### Быстрый старт (3 шага)

1. **Скачайте плагин**
   - Скачайте `MiniBoardGames.jar` из [Releases](https://github.com/Mukller/MiniBoardGames-3.0.0/releases)

2. **Установите в сервер**
   ```bash
   cp MiniBoardGames.jar /path/to/server/plugins/
   ```

3. **Перезапустите сервер**
   ```bash
   # Полный перезапуск (рекомендуется при первой установке)
   /stop
   # Запустите сервер снова
   ```

### Детальная инструкция

После первого запуска плагин автоматически создаст:
- 📁 `plugins/MiniBoardGames/` — главная папка плагина
- ⚙️ `plugins/MiniBoardGames/config.yml` — основные настройки
- 🎮 `plugins/MiniBoardGames/games/` — конфигурации всех мини-игр
- 💾 `plugins/MiniBoardGames/miniboardgames.db` — база данных игровой статистики

---

## 🎮 Основные команды

### Для игроков

| Команда | Описание | Пример |
|---------|---------|---------|
| `/mbg help` | Справка по плагину | `/mbg help` |
| `/mbg play <game>` | Начать мини-игру | `/mbg play 2048` |
| `/mbg list` | Список всех доступных игр | `/mbg list` |
| `/mbg stats` | Просмотр вашей статистики | `/mbg stats` |
| `/mbg profile <player>` | Профиль другого игрока | `/mbg profile Steve` |

### Для администраторов

| Команда | Описание | Требование |
|---------|---------|-----------|
| `/mbg reload` | Перезагрузить конфигурацию | `mbg.admin` |
| `/mbg reset <player>` | Сбросить статистику игрока | `mbg.admin` |
| `/mbg debug` | Включить/отключить режим отладки | `mbg.admin` |

### Система разрешений (Permissions)

```
mbg.play              - Право на игру в мини-игры
mbg.play.<game>       - Право на конкретную игру (например, mbg.play.2048)
mbg.stats             - Просмотр статистики
mbg.admin             - Все административные команды
mbg.reload            - Перезагрузка конфигов
```

---

## ⚙️ Конфигурация

### Основной конфиг (`config.yml`)

```yaml
# Основные настройки плагина
plugin:
  debug: false                    # Включить режим отладки
  language: ru_RU                 # Язык интерфейса (ru_RU, en_US)
  auto-save-interval: 300         # Интервал сохранения в секундах

# Настройки игр
games:
  enabled-games:
    - "2048"
    - "flappybird"
    - "battleship"
    - "coinflip"
    - "checkers"
    - "connect4"
    # Добавляйте/удаляйте игры по необходимости

# Система наград
rewards:
  enabled: true
  money-per-win: 100              # Денег за победу (если используется Vault)
  exp-per-win: 50                 # Опыта за победу
  multiplier-per-streak: 1.5      # Множитель за серию побед

# Настройки базы данных
database:
  type: sqlite                    # Тип БД (sqlite или mysql)
  # Если используете MySQL:
  # host: localhost
  # port: 3306
  # name: minigames
  # user: root
  # password: password
```

### Конфигурация отдельных игр

Каждая игра имеет свой файл конфигурации в папке `games/`:

**Пример: `games/2048_config.yml`**
```yaml
enabled: true
min-players: 1
max-players: 1
time-limit: 600                   # Секунды
difficulty: medium                # easy, medium, hard
```

**Пример: `games/battleship_config.yml`**
```yaml
enabled: true
min-players: 2
max-players: 2
board-size: 10x10
time-per-move: 30
```

---

## 🎮 Доступные игры

| Игра | Игроков | Описание |
|------|---------|---------|
| **2048** | 1 | Логическая головоломка - объединяйте плитки |
| **FlappyBird** | 1 | Аркада - пролетите между трубами |
| **BattleShip** | 2 | Стратегия - найдите корабли противника |
| **CoinFlip** | 2 | Азартная - угадайте сторону монеты |
| **Checkers** | 2 | Стратегия - классические шашки |
| **Connect4** | 2 | Логика - выстройте 4 в ряд |
| **BlackJack** | 1-4 | Карточная - наберите 21 пункт |
| **Hearthstone** | 2 | Карточная - коллекционная карточная игра |
| **HigherLower** | 1 | Логика - угадайте следующую карту |
| **CandyCrush** | 1 | Матч-3 - собирайте конфеты |
| **FabulousFred** | 1-2 | Платформер - пройдите все уровни |

И многие другие...

---

## 📊 Система статистики

Плагин отслеживает:
- 📈 Количество побед/проигрышей
- ⏱️ Время проведённое в играх
- 🏆 Достижения и рекорды
- 💰 Полученные награды
- 🎯 Рейтинговые баллы

Статистика сохраняется в базе данных и доступна через команды:
```
/mbg stats              - Ваша статистика
/mbg profile <player>   - Профиль игрока
```

---

## 🤝 Контрибьютинг

Мы приветствуем вклад от разработчиков! Вот как принять участие:

### Процесс внесения изменений

1. **Форкните репозиторий**
   ```bash
   git clone https://github.com/YOUR_USERNAME/MiniBoardGames-3.0.0.git
   cd MiniBoardGames-3.0.0
   ```

2. **Создайте ветку для фичи**
   ```bash
   git checkout -b feature/AmazingFeature
   ```

3. **Внесите изменения и закоммитьте их**
   ```bash
   git add .
   git commit -m 'Add: описание вашего изменения'
   ```

4. **Отправьте в ваш форк**
   ```bash
   git push origin feature/AmazingFeature
   ```

5. **Откройте Pull Request** на GitHub

### Руководство по стилю

- Следуйте существующему стилю кода
- Добавляйте комментарии к сложным функциям
- Обновляйте документацию при необходимости
- Пишите понятные сообщения в коммитах

### Типы PR

- 🐛 **Баг фиксы** — исправления ошибок
- ✨ **Фичи** — новые возможности
- 📚 **Документация** — улучшения документации
- 🔧 **Рефакторинг** — улучшение кода

---

## 🐛 Сообщить об ошибках

Нашли баг? Помогите нам его исправить!

### Как создать хороший issue

1. **Проверьте**, что бага нет в существующих issues
2. **Опишите проблему** максимально подробно
3. **Приложите логи** (`plugins/MiniBoardGames/debug.log`)
4. **Укажите версию** Minecraft, Java и плагина
5. **Шаги воспроизведения** - как повторить баг

### Шаблон issue

```markdown
## Описание
Подробное описание ошибки

## Шаги воспроизведения
1. Сделайте то-то
2. Затем то-то
3. Произойдёт ошибка

## Ожидаемое поведение
Что должно было произойти

## Информация о системе
- Версия Minecraft: 1.19.2
- Версия Java: 17
- Версия плагина: 3.0.0
- Логи: [приложите лог]

## Дополнительный контекст
Любая другая информация
```

Создать issue: [GitHub Issues](https://github.com/Mukller/MiniBoardGames-3.0.0/issues)

---

## 📖 Документация

- [Полное руководство пользователя](docs/USER_GUIDE.md)
- [Руководство администратора](docs/ADMIN_GUIDE.md)
- [Руководство разработчика](docs/DEVELOPER_GUIDE.md)
- [FAQ - Часто задаваемые вопросы](docs/FAQ.md)

---

## 🔐 Безопасность

Если вы обнаружили уязвимость безопасности, пожалуйста **не публикуйте её в issues**. Вместо этого напишите на [security@example.com](mailto:security@example.com).

---

## 📝 Лицензия

Этот проект лицензирован под **MIT License** — см. файл [LICENSE](LICENSE) для полного текста.

**Кратко:**
- ✅ Вы можете использовать в личных и коммерческих целях
- ✅ Вы можете изменять и распространять код
- ⚠️ Вы должны указывать авторов оригинального кода
- ⚠️ Автор не несёт ответственность за ущерб

---

## 👨‍💻 Автор и соавторы

| Роль | Контакт |
|------|---------|
| **Создатель** | [Mukller](https://github.com/Mukller) |
| **Главный разработчик** | [@Mukller](https://github.com/Mukller) |

### Спасибо всем контрибьюторам! 🙏

---

## 📞 Связь и поддержка

- 💬 [Discord сервер](https://discord.gg/example) (если есть)
- 🐛 [Багрепорты](https://github.com/Mukller/MiniBoardGames-3.0.0/issues)

---

## 🎉 Благодарности

Спасибо за использование **MiniBoardGames**! Если вам нравится плагин, звезда ⭐ на GitHub очень поможет!

<div align="center">

**Made with ❤️ by Mukller**

[⬆ вернуться в начало](#miniboardgames-300)

</div>

</details>
