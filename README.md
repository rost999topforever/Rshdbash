```markdown
# Rshdbash Framework

**Bash framework created by Rost999**  
*Russian version below | Русская версия ниже*

---

## Official Release v1.2 "RAW POWER"

After 7 development iterations, Rshdbash reaches new level with raw terminal control and interactive capabilities.

### 🆕 What's New in v1.2

#### 🔥 Raw Terminal Control
```bash
rawd          # Enable raw mode (no echo)
srawed SECONDS # Temporary raw mode with timeout  
saved         # Restore terminal safely
Deadraw       # Ultimate raw mode (use with caution!)
```

🎮 Interactive Examples

```bash
# Instant key detection
rawd
key=$(dd bs=1 count=1 2>/dev/null)
saved

# Quick menu
srawed 5
echo "Press 1-3 for options..."
```

🎯 Core Philosophy

Rshdbash enhances Bash by:

· Simplifying Bash scripting for beginners
· Accelerating prototyping with one-liners
· Maintaining full Bash compatibility
· Adding raw terminal power for interactive apps

---

📚 Core Functions

🧮 Mathematics

```bash
count X Y          # Add numbers
ewo VAR X OP Y     # Any math operation: ewo result 5 + 3
```

⌨️ Input/Output

```bash
readP "text" VAR   # Prompt input
exo "text"         # Print with newline
Exo "text"         # Print without newline  
slexo "text" DELAY # Animated typing
```

🔄 Control Structures

```bash
FIF "condition" "true_action" "false_action"  # Full if-else
WH "condition" "action"                       # While loop
WHT "action"                                 # Infinite loop
FOR "items" "action"                         # For each
FORR START END "action"                      # Range loop
```

🎲 Randomization

```bash
randomer VAR MAX MIN    # Random number
rchos "items" VAR       # Random choice from list
```

📁 File Operations

```bash
prog FILE              # Create file
proger FILE            # Append to file
DOit SCRIPT            # Execute script
```

⚡ System Utilities

```bash
uns VAR                # Unset variable
allK                   # Emergency kill all processes
timer                  # Stopwatch
home                   # Go to home directory
HCall                  # Clear history
```

🎪 Entertainment

```bash
smile N               # Smiley animation
mow N                 # Cow animation
```

🎬 Animation System (v1.1+)

```bash
gif DELAY FRAME1 FRAME2 FRAME3 FRAME4      # Fullscreen animation
anim DELAY STATE1 STATE2 STATE3 STATE4     # Smooth transitions
fill EXTENSION                             # Find files by extension
YoN "question"                             # Yes/No confirmation
TRAPED "command"                           # Signal handling
```

---

🚀 Usage

Interactive Shell

```bash
./rshdbash.sh
```

As Library

```bash
source rshdbash.sh

randomer number 100 1
FIF "\$number -gt 50" "exo 'Greater than 50'" "exo 'Less or equal'"
```

---

💡 Examples

Educational

```bash
FOR "1 2 3 4 5" "FIF \"\\$i -gt 3\" \"exo 'Greater than 3'\" \"exo 'Less than 4'\""
```

Practical

```bash
FIF "-d /backup" "tar -czf backup.tar.gz /data" "mkdir /backup"
```

Admin Tasks

```bash
WHT "FIF '! systemctl is-active nginx' 'systemctl restart nginx' 'exo ✅'; sleep 30"
```

Interactive Apps (v1.2)

```bash
# Quick clicker
rawd
score=0
while true; do
    key=$(dd bs=1 count=1 2>/dev/null)
    [[ "$key" == " " ]] && ((score++))
    [[ "$key" == "q" ]] && break
    printf "\rScore: %d" $score
done
saved
```

---

⚠️ Important Warnings

· allK terminates ALL user processes - use with extreme caution!
· Raw mode functions (rawd, Deadraw) can break terminal - use saved to restore
· Always test in safe environment first

---

📋 System Requirements

· Bash 3.2+
· Any Unix-like system

---

📄 License

GPL-3.0

🙏 Acknowledgments

Thanks to DeepSeek for testing assistance.

---

Rshdbash v1.2 - Powerful, interactive Bash framework with raw terminal control!

---

Фреймворк Rshdbash

Фреймворк для Bash, созданный Rost999

---

Официальный релиз v1.2 "RAW POWER"

После 7 итераций разработки Rshdbash выходит на новый уровень с контролем терминала и интерактивными возможностями.

🆕 Что нового в v1.2

🔥 Контроль терминала

```bash
rawd          # Включить raw mode (без echo)
srawed СЕКУНДЫ # Временный raw mode с таймаутом
saved         # Безопасное восстановление терминала
Deadraw       # Максимальный raw mode (используйте осторожно!)
```

🎮 Интерактивные примеры

```bash
# Мгновенное определение клавиш
rawd
key=$(dd bs=1 count=1 2>/dev/null)
saved

# Быстрое меню
srawed 5
echo "Нажмите 1-3 для выбора..."
```

🎯 Философия

Rshdbash улучшает Bash через:

· Упрощение скриптинга для новичков
· Ускорение прототипирования однострочниками
· Сохранение совместимости с Bash
· Добавление контроля терминала для интерактивных приложений

---

📚 Основные функции

🧮 Математика

```bash
count X Y          # Сложение чисел
ewo VAR X OP Y     # Любые операции: ewo результат 5 + 3
```

⌨️ Ввод-вывод

```bash
readP "текст" VAR  # Ввод с подсказкой
exo "текст"        # Вывод с переносом
Exo "текст"        # Вывод без переноса
slexo "текст" ЗАДЕРЖКА # Анимированный вывод
```

🔄 Управляющие структуры

```bash
FIF "условие" "действие_истина" "действие_ложь"  # Полное ветвление
WH "условие" "действие"                          # Цикл while
WHT "действие"                                   # Бесконечный цикл
FOR "элементы" "действие"                        # Перебор элементов
FORR НАЧАЛО КОНЕЦ "действие"                     # Перебор диапазона
```

🎲 Случайности

```bash
randomer VAR МАКС МИН    # Случайное число
rchos "элементы" VAR     # Случайный выбор
```

📁 Файловые операции

```bash
prog ФАЙЛ               # Создание файла
proger ФАЙЛ             # Добавление в файл
DOit СКРИПТ             # Запуск скрипта
```

⚡ Системные утилиты

```bash
uns VAR                 # Очистка переменной
allK                    # Аварийное завершение процессов
timer                   # Секундомер
home                    # Переход в домашнюю директорию
HCall                   # Очистка истории
```

🎪 Развлекательные

```bash
smile N                # Анимация смайликов
mow N                  # Анимация коровки
```

🎬 Система анимации (v1.1+)

```bash
gif ЗАДЕРЖКА КАДР1 КАДР2 КАДР3 КАДР4    # Полноэкранная анимация
anim ЗАДЕРЖКА СОСТОЯНИЕ1 СОСТ2 СОСТ3 СОСТ4 # Плавные переходы
fill РАСШИРЕНИЕ                          # Поиск файлов
YoN "вопрос"                             # Подтверждение Да/Нет
TRAPED "команда"                         # Обработка сигналов
```

---

🚀 Использование

Интерактивная оболочка

```bash
./rshdbash.sh
```

Как библиотека

```bash
source rshdbash.sh

randomer число 100 1
FIF "\$число -gt 50" "exo 'Больше 50'" "exo 'Меньше или равно'"
```

---

💡 Примеры

Образовательные

```bash
FOR "1 2 3 4 5" "FIF \"\\$i -gt 3\" \"exo 'Больше 3'\" \"exo 'Меньше 4'\""
```

Практические

```bash
FIF "-d /backup" "tar -czf backup.tar.gz /data" "mkdir /backup"
```

Админские

```bash
WHT "FIF '! systemctl is-active nginx' 'systemctl restart nginx' 'exo ✅'; sleep 30"
```

Интерактивные приложения (v1.2)

```bash
# Быстрый кликер
rawd
счёт=0
while true; do
    key=$(dd bs=1 count=1 2>/dev/null)
    [[ "$key" == " " ]] && ((счёт++))
    [[ "$key" == "q" ]] && break
    printf "\rСчёт: %d" $счёт
done
saved
```

---

⚠️ Важные предупреждения

· allK завершает ВСЕ процессы пользователя - используйте крайне осторожно!
· Функции raw mode (rawd, Deadraw) могут сломать терминал - используйте saved для восстановления
· Всегда тестируйте в безопасной среде

---

📋 Системные требования

· Bash 3.2+
· Любая Unix-подобная система

---

📄 Лицензия

GPL-3.0

🙏 Благодарности

Спасибо DeepSeek за помощь в тестировании.

---

Rshdbash v1.2 - Мощный интерактивный фреймворк для Bash с контролем терминала!

```
