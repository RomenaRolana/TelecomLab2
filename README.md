# TelecomLab2
1. Функція generateRandomSequence(length)
Ця функція призначена для генерації випадкової послідовності нулів та одиниць заданої довжини. Вона використовує метод Array.from для створення масиву заданої довжини length, кожен елемент якого заповнюється випадковим числом (0 або 1). Це досягається за допомогою функції Math.floor(Math.random() * 2), яка генерує ціле число в діапазоні від 0 до 1.

2. Функція interleave(sequence, rows, cols, permute)
Функція interleave призначена для інтерлівування вхідної послідовності бітів, розташовуючи біти в двовимірний масив (матрицю) і використовуючи зазначений порядок перестановки стовпців. Вона приймає чотири параметри:


sequence: Вхідна послідовність бітів.

rows: Кількість рядків у матриці.

cols: Кількість стовпців у матриці.

permute: Масив, який визначає порядок перестановки стовпців.

Спочатку функція створює матрицю, заповнюючи її рядками з вхідної послідовності. Потім виконує перестановку стовпців згідно з масивом permute та збирає результат у новий масив interleaved.

3. Функція deinterleave(sequence, rows, cols, permute)
Ця функція виконує обернену операцію до інтерлівування — деінтерлівування. Вона приймає ті ж параметри, що й interleave, і виконує зворотнє впорядкування елементів з інтерлійованої послідовності до їх початкового розташування. Спочатку створюється матриця з null-значеннями, далі за допомогою оберненого порядку permute елементи розміщуються на свої позиції в матриці, а потім послідовно зчитуються рядками для формування вихідної послідовності.

4. Функція compareSequences(original, deinterleaved)
Функція compareSequences порівнює дві послідовності (оригінальну та деінтерлійовану) на ідентичність. Вона повертає true, якщо всі елементи в обох послідовностях збігаються, інакше — false. Це корисно для перевірки, чи відновлено оригінальну послідовність правильно після інтерлівування та деінтерлівування.

5. Функція generateAndDisplaySequences()
Ця функція інтегрує всі вищезазначені функції для демонстрації їх роботи. Вона генерує випадкову послідовність, застосовує до неї інтерлівування, далі виконує деінтерлівування та перевіряє, чи деінтерлійована послідовність збігається з оригінальною. Результати цих операцій відображаються в HTML-елементі div з ID results.

Ці функції дозволяють відтворити та перевірити процеси інтерлівування і деінтерлівування, які є важливими у системах зв'язку для підвищення стійкості передачі даних до помилок, спричинених завмиранням сигналу чи іншими перешкодами.
