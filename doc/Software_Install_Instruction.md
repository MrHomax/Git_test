# Встановлення програмного забезпечення для курсу «Основи програмування для інженерів»

## 1. Призначення інструкції

Ця інструкція призначена для підготовки комп'ютера до виконання лабораторних робіт та інших завдань з курсу.

Потрібно встановити:

- **Python 3.14.x (64-bit)**;
- Python-пакети **NumPy**, **Matplotlib**, **SciPy**;
- **Tkinter** для створення графічних інтерфейсів;
- **Visual Studio Code**;
- розширення **Python** для Visual Studio Code;
- **Git for Windows**.

> **Операційна система:** інструкція розрахована насамперед на Windows 10/11 та звичайний 64-бітний комп'ютер з процесором Intel або AMD.

> **Важливо:** завантажуйте програми лише з офіційних сайтів, посилання на які наведені нижче.

---

# 2. Що і звідки завантажувати

| Програма / компонент | Що завантажити | Офіційне джерело |
|---|---|---|
| Python | Python 3.14.x, Windows installer (64-bit) | [Python.org — Windows](https://www.python.org/downloads/windows/) |
| NumPy | Встановлюється через `pip` | Python Package Index / `pip` |
| Matplotlib | Встановлюється через `pip` | Python Package Index / `pip` |
| SciPy | Встановлюється через `pip` | Python Package Index / `pip` |
| Tkinter | Окремо завантажувати не потрібно | Входить до стандартної інсталяції Python |
| Visual Studio Code | Windows User Installer, x64 | [VS Code — Download](https://code.visualstudio.com/download) |
| Python extension | Extension «Python» від Microsoft | [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=ms-python.python) |
| Git | Git for Windows, x64 | [Git for Windows](https://git-scm.com/install/windows) |

---

# 3. Встановлення Python

## 3.1. Завантаження

Відкрийте офіційну сторінку:

**https://www.python.org/downloads/windows/**

У розділі Python 3.14.x знайдіть:

**Windows installer (64-bit)**

Для звичайного комп'ютера з Windows на процесорі Intel або AMD потрібна саме версія **64-bit**.

Не завантажуйте:

- `Windows embeddable package`;
- `Windows installer (ARM64)`, якщо у вас звичайний Intel/AMD комп'ютер;
- `Windows installer (32-bit)`, якщо у вас 64-бітна Windows.

На момент підготовки цієї інструкції актуальним стабільним релізом Python 3 є **Python 3.14.7**.

## 3.2. Запуск інсталятора

Після завантаження запустіть файл встановлення Python.

На першому екрані інсталятора:

**обов'язково встановіть прапорець:**

> ☑ Add python.exe to PATH

Після цього натисніть:

> **Install Now**

### Чому потрібно встановити `Add python.exe to PATH`?

Це дозволить запускати Python та `pip` безпосередньо з Command Prompt, PowerShell або Windows Terminal.

Наприклад:

```text
python --version
```

та

```text
python -m pip install numpy
```

Якщо прапорець не встановити, надалі можуть виникнути проблеми із запуском Python з командного рядка.

## 3.3. Завершення встановлення

Дочекайтеся завершення встановлення.

Після появи повідомлення про успішне встановлення натисніть:

> **Close**

---

# 4. Перевірка встановлення Python

Відкрийте **Windows Terminal**, **PowerShell** або **Command Prompt (CMD)**.

Найпростіший спосіб:

1. натисніть клавішу **Windows**;
2. введіть `cmd`;
3. натисніть **Enter**.

Виконайте:

```text
python --version
```

Має з'явитися приблизно:

```text
Python 3.14.7
```

Версія може бути новішою в межах Python 3.14.x — це нормально.

Також перевірте `pip`:

```text
python -m pip --version
```

Має з'явитися інформація про версію `pip` та каталог його встановлення.

## Якщо команда `python` не працює

Спробуйте:

```text
py --version
```

Якщо команда `py` працює, але `python` не працює, найчастіше проблема пов'язана з PATH.

У такому випадку рекомендується перевірити, чи під час встановлення Python було встановлено прапорець:

> Add python.exe to PATH

---

# 5. Встановлення NumPy, Matplotlib та SciPy

## 5.1. Оновлення pip

У тому самому вікні CMD або Terminal виконайте:

```text
python -m pip install --upgrade pip
```

Дочекайтеся завершення операції.

## 5.2. Встановлення необхідних пакетів

Виконайте одну команду:

```text
python -m pip install numpy matplotlib scipy
```

Після завершення має з'явитися повідомлення про успішне встановлення пакетів.

### Що встановлюється?

- **NumPy** — робота з масивами та числовими обчисленнями;
- **Matplotlib** — побудова графіків;
- **SciPy** — наукові та інженерні обчислення.

> **Не потрібно завантажувати NumPy, Matplotlib або SciPy окремими `.exe`-файлами.** Для цього курсу вони встановлюються через менеджер пакетів Python — `pip`.

---

# 6. Tkinter

**Tkinter окремо встановлювати через `pip` не потрібно.**

Tkinter входить до стандартної інсталяції Python для Windows.

Для перевірки виконайте:

```text
python -m tkinter
```

Якщо все встановлено правильно, відкриється невелике тестове вікно Tk.

Після перевірки це вікно можна закрити.

> **Не виконуйте:** `pip install tkinter`

Tkinter не встановлюється таким способом у стандартному середовищі Python.

---

# 7. Перевірка всіх Python-пакетів

Після встановлення NumPy, Matplotlib, SciPy виконайте:

```text
python -c "import numpy, matplotlib, scipy, tkinter; print('All Python packages are OK')"
```

Якщо все правильно, з'явиться:

```text
All Python packages are OK
```

Якщо з'явилося повідомлення про помилку, **не переходьте до наступного кроку**, а спочатку усуньте проблему.

---

# 8. Встановлення Visual Studio Code

## 8.1. Завантаження

Відкрийте офіційну сторінку:

**https://code.visualstudio.com/download**

У розділі Windows виберіть:

> **User Installer → x64**

Для більшості студентів це рекомендований варіант.

Не потрібно завантажувати:

- ARM64 — якщо у вас звичайний Intel/AMD комп'ютер;
- `.zip` версію;
- Insiders Edition.

## 8.2. Встановлення

Запустіть завантажений `.exe`-файл.

Пройдіть стандартну процедуру встановлення.

Рекомендується залишити стандартний каталог встановлення.

Під час встановлення зверніть увагу на додаткові опції.

Якщо вони доступні, рекомендується встановити:

> ☑ Add to PATH

та

> ☑ Add "Open with Code" action

Після цього заверште встановлення.

Запустіть **Visual Studio Code**.

---

# 9. Встановлення Python Extension для VS Code

Сам Visual Studio Code **не містить Python**. Python та VS Code — це два окремі компоненти.

Для роботи з Python потрібно встановити розширення Python.

## 9.1. Встановлення через VS Code

1. Запустіть **Visual Studio Code**.
2. У лівій частині вікна натисніть **Extensions**.
3. Або натисніть:

```text
Ctrl + Shift + X
```

4. У полі пошуку введіть:

```text
Python
```

5. Знайдіть розширення:

> **Python**  
> **Microsoft**

6. Натисніть:

> **Install**

Офіційна сторінка розширення:

https://marketplace.visualstudio.com/items?itemName=ms-python.python

Розширення Python забезпечує, зокрема:

- підсвічування та аналіз Python-коду;
- автодоповнення та IntelliSense;
- запуск Python-програм;
- вибір інтерпретатора Python;
- налагодження програм;
- підтримку тестування.

> Окремо встановлювати Pylance або Python Debugger на початковому етапі не потрібно. Необхідні компоненти можуть встановлюватися та використовуватися разом із Python extension.

---

# 10. Вибір інтерпретатора Python у VS Code

Після встановлення Python extension потрібно повідомити VS Code, яку саме версію Python використовувати.

## Спосіб 1 — через Command Palette

Натисніть:

```text
Ctrl + Shift + P
```

Введіть:

```text
Python: Select Interpreter
```

Виберіть цю команду.

У списку знайдіть встановлений Python, наприклад:

```text
Python 3.14.7
```

та виберіть його.

## Спосіб 2 — через Status Bar

У нижній частині вікна VS Code може відображатися вибраний Python interpreter.

Натисніть на нього та виберіть:

```text
Python 3.14.7
```

> Якщо VS Code не знаходить Python автоматично, переконайтеся, що Python дійсно встановлений та команда `python --version` працює у CMD.

---

# 11. Перша програма у VS Code

Створіть окрему папку для навчальних програм.

Наприклад:

```text
Documents
└── Python_Projects
```

У VS Code відкрийте:

> **File → Open Folder...**

та виберіть папку `Python_Projects`.

## Створення Python-файлу

Створіть файл:

```text
hello.py
```

Введіть:

```python
print("Hello, Python!")
```

Збережіть файл.

---

# 12. Запуск програми

У правому верхньому куті редактора натисніть кнопку запуску Python-файлу.

Або відкрийте Terminal у VS Code та виконайте:

```text
python hello.py
```

Очікуваний результат:

```text
Hello, Python!
```

Якщо програма запускається — Python, VS Code та Python extension працюють правильно.

---

# 13. Перевірка відлагодження (Debugger)

VS Code дозволяє виконувати програму покроково та перевіряти значення змінних.

Замініть код у `hello.py` на:

```python
a = 10
b = 20

result = a + b

print(result)
```

## Встановлення breakpoint

1. Встановіть курсор на рядок:

```python
result = a + b
```

2. Натисніть ліворуч від номера цього рядка.
3. Має з'явитися червона крапка — **breakpoint**.

## Запуск debugger

Натисніть:

```text
F5
```

Програма зупиниться на breakpoint.

Під час налагодження можна:

- виконувати програму покроково;
- переглядати значення змінних;
- бачити стек викликів;
- продовжувати виконання;
- зупиняти програму.

Якщо програма зупиняється на breakpoint — **Python Debugger працює правильно**.

---

# 14. Встановлення Git

## 14.1. Завантаження

Відкрийте офіційну сторінку:

**https://git-scm.com/install/windows**

Завантажте:

> **Git for Windows — x64**

Для звичайного Intel/AMD комп'ютера потрібна версія x64.

## 14.2. Встановлення

Запустіть завантажений інсталятор.

У більшості випадків можна залишати стандартні параметри.

### Важливий пункт — PATH

Під час встановлення з'явиться налаштування на кшталт:

> **Adjusting your PATH environment**

Рекомендується залишити варіант:

> **Git from the command line and also from 3rd-party software**

Це дозволить використовувати Git:

- у Command Prompt;
- у PowerShell;
- у Windows Terminal;
- у Visual Studio Code.

### Редактор Git

Якщо інсталятор запропонує вибрати редактор за замовчуванням, можна вибрати:

> **Visual Studio Code**

Якщо ви не впевнені, який варіант вибрати, залиште запропонований інсталятором параметр.

Для решти параметрів можна використовувати значення за замовчуванням.

Завершіть встановлення Git.

---

# 15. Перевірка Git

Після встановлення Git відкрийте **нове** вікно CMD або Terminal.

Виконайте:

```text
git --version
```

Має з'явитися приблизно:

```text
git version 2.55.0
```

Версія може бути новішою — це нормально.

> Якщо команда `git` не розпізнається, закрийте CMD/Terminal та відкрийте його знову. Зміни PATH можуть бути доступними лише в нових процесах.

---

# 16. Перевірка Git у VS Code

Відкрийте папку `Python_Projects` у VS Code.

У лівій частині вікна знайдіть:

> **Source Control**

або натисніть:

```text
Ctrl + Shift + G
```

Якщо VS Code бачить встановлений Git, система контролю версій буде доступна без додаткового встановлення розширення Git.

---

# 17. Фінальна перевірка всього програмного середовища

Після встановлення всіх компонентів рекомендується виконати повну перевірку.

## 17.1. Python

У CMD:

```text
python --version
```

Очікується:

```text
Python 3.14.x
```

## 17.2. pip

```text
python -m pip --version
```

## 17.3. NumPy

```text
python -c "import numpy; print('NumPy OK')"
```

## 17.4. Matplotlib

```text
python -c "import matplotlib; print('Matplotlib OK')"
```

## 17.5. SciPy

```text
python -c "import scipy; print('SciPy OK')"
```

## 17.6. Tkinter

```text
python -m tkinter
```

Має відкритися тестове вікно.

## 17.7. Git

```text
git --version
```

---

# 18. Фінальна комплексна перевірка

Можна виконати всі перевірки Python однією командою:

```text
python -c "import numpy, matplotlib, scipy, tkinter; print('Python environment OK')"
```

Очікуваний результат:

```text
Python environment OK
```

Після цього перевірте Git:

```text
git --version
```

Якщо обидві перевірки виконуються без помилок, базове програмне середовище готове.

---

# 19. Підсумковий список встановленого ПЗ

Після виконання інструкції на комп'ютері мають бути встановлені:

- [x] Python 3.14.x (64-bit)
- [x] pip
- [x] NumPy
- [x] Matplotlib
- [x] SciPy
- [x] Tkinter
- [x] Visual Studio Code
- [x] Python extension for VS Code
- [x] Python Debugger для VS Code
- [x] Git for Windows

---

# 20. Рекомендована структура папок для навчання

Для виконання лабораторних робіт рекомендується створити окрему папку:

```text
Documents
└── Python_Projects
    ├── lab01
    ├── lab02
    ├── lab03
    └── ...
```

Кожну лабораторну роботу бажано зберігати в окремій папці.

Наприклад:

```text
Python_Projects
└── lab01
    ├── main.py
    └── ...
```

Це особливо важливо при подальшому використанні Git.

---

# 21. Часті проблеми

## Проблема 1. `python is not recognized...`

Якщо після встановлення команда

```text
python --version
```

не працює:

1. закрийте CMD/Terminal;
2. відкрийте його знову;
3. повторіть команду.

Якщо проблема залишилася, перевірте:

```text
py --version
```

Якщо `py` працює, але `python` — ні, перевірте PATH або повторіть встановлення Python з увімкненою опцією:

> **Add python.exe to PATH**

---

## Проблема 2. `pip` не працює

Не обов'язково використовувати команду:

```text
pip install ...
```

Замість цього використовуйте:

```text
python -m pip install ...
```

Наприклад:

```text
python -m pip install numpy matplotlib scipy
```

---

## Проблема 3. VS Code не знаходить Python

Виконайте:

```text
python --version
```

у CMD.

Якщо команда працює, у VS Code виконайте:

```text
Ctrl + Shift + P
```

→

```text
Python: Select Interpreter
```

та виберіть встановлений Python.

---

## Проблема 4. `ModuleNotFoundError: No module named 'numpy'`

Це означає, що NumPy не встановлений у тому Python-середовищі, яке використовується для запуску програми.

Виконайте:

```text
python -m pip install numpy
```

Аналогічно:

```text
python -m pip install matplotlib
```

```text
python -m pip install scipy
```

Після цього переконайтеся, що у VS Code вибраний той самий Python interpreter.

---

## Проблема 5. Git не знаходиться у VS Code

Спочатку перевірте Git у CMD:

```text
git --version
```

Якщо команда працює, перезапустіть VS Code.

Якщо команда не працює, можливо, Git був встановлений без додавання його до PATH. У такому випадку можна повторно запустити інсталятор Git та перевірити параметр:

> **Git from the command line and also from 3rd-party software**

---

# 22. Важливі зауваження

### Не встановлюйте зайве програмне забезпечення

Для виконання цього курсу **не потрібно встановлювати**:

- Anaconda;
- Miniconda;
- окремий Python IDE;
- окремий debugger;
- окремий Git GUI.

Для роботи достатньо:

**Python + pip + NumPy + Matplotlib + SciPy + Tkinter + VS Code + Python extension + Git.**

### Не завантажуйте Python-пакети з випадкових сайтів

NumPy, Matplotlib та SciPy не потрібно шукати на сторонніх сайтах.

Використовуйте:

```text
python -m pip install numpy matplotlib scipy
```

---

# 23. Офіційна документація

- [Python — офіційна сторінка завантаження для Windows](https://www.python.org/downloads/windows/)
- [Python 3.14.7](https://www.python.org/downloads/release/python-3147/)
- [Visual Studio Code — завантаження](https://code.visualstudio.com/download)
- [Python у Visual Studio Code — офіційна документація](https://code.visualstudio.com/docs/languages/python)
- [Python extension для VS Code](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
- [Git for Windows — завантаження](https://git-scm.com/install/windows)

---

## Готове середовище

Після успішного завершення всіх етапів студент повинен мати робоче середовище:

```text
                    ┌─────────────────────┐
                    │   Visual Studio Code│
                    └──────────┬──────────┘
                               │
                         Python Extension
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Python 3.14.x     │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              │                │                │
              ▼                ▼                ▼
           NumPy          Matplotlib          SciPy
              │
              │
              ▼
           Tkinter

                    Git ──► контроль версій
```

Цього набору достатньо для виконання програмних та лабораторних робіт курсу.
