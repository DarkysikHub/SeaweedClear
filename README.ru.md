# 🌊 SeaweedClear

[![Java](https://img.shields.io/badge/Java-8%2B-orange?logo=openjdk)](https://java.com)
[![Spigot](https://img.shields.io/badge/Spigot-1.13%2B-yellow)](https://www.spigotmc.org)
[![Лицензия](https://img.shields.io/badge/лицензия-MIT-green.svg)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/username/repo)](https://github.com/username/repo/stargazers)
[![Discord](https://img.shields.io/discord/server_id?logo=discord&label=Discord)](https://discord.gg/invite-link)

Идеальное решение для управления водной растительностью на Minecraft-серверах. Эффективно очищает водоросли, ламинарию и морскую траву с хирургической точностью, не нагружая сервер.

## ✨ Возможности

- **Умная очистка** - Удаляет 5+ видов водных растений
- **Поддержка нескольких миров** - Работает во всех измерениях
- **Очистка по радиусу** - Удаляет растительность вокруг игроков
- **Оптимизированная производительность** - Постепенная обработка чанков
- **Отслеживание в реальном времени** - Прогресс в HUD и консоли
- **Многоязычная поддержка** - Встроенные локализации EN/RU
- **Современное API** - Полная совместимость с Spigot/Paper 1.13+

## 🛠 Установка

1. Скачайте последнюю версию `.jar` из [Releases](https://github.com/yourname/SeaweedClear/releases)
2. Поместите файл в папку `plugins/`
3. Перезапустите сервер
4. (Опционально) Отредактируйте `plugins/SeaweedClear/config.yml`

## 📋 Команды

| Команда | Описание | Права доступа |
|---------|-------------|------------|
| `/sc world <мир>` | Очистка в указанном мире | `seaweedclear.world` |
| `/sc all` | Очистка во всех мирах | `seaweedclear.all` |
| `/sc radius <размер>` | Очистка вокруг игрока | `seaweedclear.radius` |
| `/sc info` | Показать прогресс | `seaweedclear.info` |
| `/sc reload` | Перезагрузить конфиг | `seaweedclear.reload` |
| `/sc stop` | Остановить активные очистки | `seaweedclear.stop` |

## ⚙ Конфигурация

```yaml
# plugins/SeaweedClear/config.yml
language: en # en/ru
logging:
  enable: true
performance:
  chunks-per-tick: 2 # Количество обрабатываемых чанков за тик
  tick-delay: 5 # Интервал между обработкой (в тиках)
```

🌍 Локализация

Редактируйте файлы для добавления переводов:
- `messages_en.yml` (Английский)
- `messages_ru.yml` (Русский)

📜 Права доступа

```yaml
seaweedclear.world:
  description: Разрешает использование /sc world
  default: op

seaweedclear.all:
  description: Разрешает использование /sc all
  default: op
  
# ... (остальные права следуют той же схеме)
```
💻 Разработчикам

Интеграция через API:
```java
SeaweedClearAPI api = (SeaweedClearAPI) Bukkit.getPluginManager().getPlugin("SeaweedClear");
api.startCleaning(world, radius, callback);
```
📦 Зависимости

- Spigot/Paper 1.13+
- Java 8+

🚀 Планируемые функции

- [ ] Очистка по биомам
- [ ] Функция отмены действий
- [ ] Сохранение схем

📄 Лицензия

MIT License - Подробнее в LICENSE.
