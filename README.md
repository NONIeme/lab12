# Лабораторна робота №12: Робота з матрицями у Python

## Мета роботи
Метою даної лабораторної роботи є навчитися працювати з матрицями у Python, реалізувати основні операції над матрицями, такі як додавання елементів, транспонування, множення, перевірка симетричності, обертання, "сплющення" та отримання діагоналі.

## Опис завдання
1. Реалізація класу `Matrix` з методами для створення та маніпуляції матрицями.
2. Створення методів для додавання елементів до матриці, обчислення суми рядків, транспонування матриці, множення матриць, перевірки симетричності, обертання на 90 градусів за годинниковою стрілкою, "сплющення" матриці в один список та отримання діагоналі.
3. Реалізація статичного методу для створення матриці з списку списків.

## Виконання роботи
### Кроки виконання
1. Кожна лабораторна робота повинна бути завантажена в окрему папку на GitHub.
2. Назва папки повинна містити номер лабораторної роботи (наприклад, `lab12`).
3. В кожній папці повинні бути присутні наступні файли:
   - Основний код програми (`main.py`).
   - README файл з детальним поясненням.

### Структура проекту
lab12
-├── student_main.py
-├── README.md


### Опис файлів
- **main.py**: Основний код програми, що містить визначення класу `Matrix` та його методів.
- **README.md**: Файл з детальним поясненням.

### Опис основних класів та методів
- **Matrix**: Клас для роботи з матрицями.
  - **\_\_init\_\_(self, rows, columns)**: Ініціалізує матрицю розміром `rows x columns` з нульовими значеннями.
  - **add_element(self, row, column, value)**: Додає значення `value` до елементу в позиції (`row`, `column`).
  - **sum_of_rows(self)**: Повертає список з сумами кожного рядка матриці.
  - **transpose(self)**: Повертає транспоновану матрицю.
  - **multiply_by(self, other)**: Множить поточну матрицю на іншу матрицю `other` та повертає результат.
  - **is_symmetric(self)**: Перевіряє, чи є матриця симетричною.
  - **rotate_right(self)**: Обертає матрицю на 90 градусів за годинниковою стрілкою.
  - **flatten(self)**: Повертає "сплющену" матрицю у вигляді одного списку.
  - **diagonal(self)**: Повертає діагональні елементи матриці.
  - **from_list(list_of_lists)**: Статичний метод для створення матриці з списку списків.

### Приклади використання
```python
# Створення матриці 3x3
matrix = Matrix(3, 3)

# Додавання елементів до матриці
matrix.add_element(0, 0, 1)
matrix.add_element(0, 1, 2)
matrix.add_element(0, 2, 3)
matrix.add_element(1, 0, 4)
matrix.add_element(1, 1, 5)
matrix.add_element(1, 2, 6)
matrix.add_element(2, 0, 7)
matrix.add_element(2, 1, 8)
matrix.add_element(2, 2, 9)

# Відображення суми рядків
print(matrix.sum_of_rows())  # Output: [6, 15, 24]

# Транспонування матриці
transposed_matrix = matrix.transpose()
print(transposed_matrix.data)  # Output: [[1, 4, 7], [2, 5, 8], [3, 6, 9]]

# Множення матриць
other_matrix = Matrix.from_list([[1, 2], [3, 4], [5, 6]])
result_matrix = matrix.multiply_by(other_matrix)
print(result_matrix.data)  # Output: [[22, 28], [49, 64], [76, 100]]

# Перевірка симетричності
print(matrix.is_symmetric())  # Output: False

# Обертання матриці
matrix.rotate_right()
print(matrix.data)  # Output: [[7, 4, 1], [8, 5, 2], [9, 6, 3]]

# "Сплющення" матриці
print(matrix.flatten())  # Output: [7, 4, 1, 8, 5, 2, 9, 6, 3]

# Отримання діагоналі
print(matrix.diagonal())  # Output: [7, 5, 3]
```

## Результати
Під час виконання роботи були успішно реалізовані всі методи для роботи з матрицями у Python. Тестування показало коректність роботи всіх методів та класу.

## Висновки
Мета роботи була досягнута. Було реалізовано декілька методів для роботи з матрицями, що включають додавання елементів, транспонування, множення, перевірку симетричності, обертання, "сплющення" та отримання діагоналі. Проблеми, що виникли під час роботи, були вирішені шляхом вивчення алгоритмів роботи з матрицями та практичного застосування їх у коді.

### Інструкції з запуску

Вимоги до середовища
- **Python версії 3.x

Команда для запуску
```
python main.py
```
