# Проект 0. Угадай число

## Оглавление  
[1. Описание проекта](#Описание проекта)  
[2. Какой кейс решаем?](#Какой-кейс-решаем)  
[3. Краткая информация о данных](#Краткая-информация-о-данных)  
[4. Этапы работы над проектом](#Этапы-работы-над-проектом)  
[5. Результаты](#Результаты)  
[6. Выводы](#Выводы)  

### Описание проекта    
Проект реализует алгоритмы для угадывания случайного числа от 1 до 100 за минимальное количество попыток. Сравниваются разные подходы: интерактивный ввод, случайный поиск и бинарный поиск.

:arrow_up:[к оглавлению](#Оглавление)

### Какой кейс решаем?    
**Задача:** Написать программу, которая эффективно угадывает число, используя подсказки "больше" или "меньше".

**Условия:**
- Число генерируется в диапазоне 1-100.
- Алгоритм должен учитывать информацию о сравнении чисел.

**Метрика качества:**  
Среднее количество попыток при 1000 запусков.

**Что практикуем:**  
- Писать чистый, структурированный код на Python.
- Реализовывать и сравнивать разные алгоритмы.

:arrow_up:[к оглавлению](#Оглавление)

### Краткая информация о данных  
- Загаданные числа генерируются с помощью `numpy.random.randint()`.
- Для воспроизводимости результатов используется фиксированный сид (`np.random.seed(1)`).

:arrow_up:[к оглавлению](#Оглавление)

### Этапы работы над проектом  
1. **Реализация трех алгоритмов:**
   - Интерактивный ввод (пользовательский вариант).
   - Случайное угадывание (`random_predict`).
   - Бинарный поиск (`game_core_v3`).

2. **Тестирование алгоритмов:**  
   Функция `score_game()` вычисляет среднее количество попыток за 1000 экспериментов.

3. **Сравнение эффективности:**  
   Анализ результатов для выбора оптимального подхода.

:arrow_up:[к оглавлению](#Оглавление)

### Результаты  
- **Случайный поиск:** ~100 попыток (в худшем случае).
- **Бинарный поиск:** 7 попыток (максимум).
- **Интерактивный режим:** Зависит от пользователя.

:arrow_up:[к оглавлению](#Оглавление)

### Выводы  
- **Бинарный поиск** — оптимальный алгоритм для данной задачи. Он сокращает диапазон возможных чисел вдвое на каждом шаге, гарантируя угадывание за логарифмическое время.
- **Случайный поиск** неэффективен для больших диапазонов.
- Проект демонстрирует важность выбора алгоритма для оптимизации времени выполнения.

:arrow_up:[к оглавлению](#Оглавление)


*[Проект_0. Игра "Угадай число"](https://github.com/ANTIOKH2/skill_ed/blob/main/project_0/game_v2.py)
