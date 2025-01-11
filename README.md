### [@sstmintgrtn_bot](https://t.me/sstmintgrtn_bot)

![@sstmintgrtn_bot](https://www.gravatar.com/avatar/7ceee8792cfff9591510a6fe04131afa?size=200&default=robohash&forcedefault=y)

Телеграм-бот создан для освоения практических навыков интеграции информационных систем и приобретения опыта совместной работы над проектом в распределённой команде.

Бот объединяет различные функции, разработанные студентами в процессе изучения дисциплины "Системная интеграция программных приложений".  
Каждая из функций должна обеспечивать взаимодействие с внешней информационной системой.

__Тестовый Телеграм-бот__ — [@sstmintgrtn_bot](https://t.me/sstmintgrtn_bot).  

__Общая группа с ботом__ — [sstmintgrtn](https://t.me/sstmintgrtn). При пуше изменений в любую ветку результаты тестов будут также публиковаться в этой группе.

---

### Локальный запуск
Для запуска проекта локально добавьте файл `.env` с ключами в корень проекта или задайте соответствующие значения в переменных окружения вашей операционной системы.

Пример содержимого файла `.env`:  
```env
LOGLEVEL=ERROR
TBOT_LOGLEVEL=ERROR
CONECTION_PGDB=
TBOTTOKEN=

EXAMPLETOKEN=1234567890
```

---

### Токены
Ссылки на информацию о создании токенов:  

- [GITHUBTOKEN](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)

---

### Добавление функций в Телеграм-бота

Уважаемые студенты, при разработке функций для бота придерживайтесь следующих рекомендаций:  
1. Код функции должен быть размещён в отдельном файле в директории **src/functions/atomic**.  
2. Каждая функция должна быть оформлена в виде класса, который наследует абстрактный класс **AtomicBotFunctionABC**.  

Необходимые атрибуты класса:  
- `commands: List[str]` — список команд, которые вызывают вашу функцию.  
- `authors: List[str]` — ваши логины на github.com.  
- `about: str` — краткое описание функции.  
- `description: str` — подробное описание функции с параметрами (если они требуются).  
- `state: bool` — статус функции (включена или отключена).  

Пример можно найти в файле **[example_bot_function.py](https://github.com/IHVH/system-integration-bot-2/blob/master/src/functions/atomic/example_bot_function.py)**.  

---

### Используемая библиотека
Изучите возможности библиотеки, используемой в проекте:  
[pyTelegramBotAPI](https://github.com/eternnoir/pyTelegramBotAPI).  
```
