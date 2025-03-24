Програма “Вгадай число”
1. Опис
Програма "Вгадай число" – це проста гра, в якій комп'ютер загадує випадкове число в діапазоні від 1 до 100, а користувач повинен вгадати це число. Програма надає підказки "Загадане число більше" або "Загадане число менше" після кожної спроби користувача.
2. Вихідний код:

import random  # Імпортуємо модуль random для генерації випадкових чисел

def guess_the_number():  # Визначаємо функцію guess_the_number, яка містить основну логіку гри
  """
  Гра "Вгадай число".
  Комп'ютер загадує випадкове число, а користувач повинен його вгадати.
  """

  secret_number = random.randint(1, 100)  # Генеруємо випадкове ціле число від 1 до 100 і зберігаємо його у змінну secret_number
  attempts = 0  # Ініціалізуємо змінну attempts для зберігання кількості спроб користувача

  print("Ласкаво просимо до гри 'Вгадай число'!")  # Виводимо вітальне повідомлення для користувача
  print("Я загадав число від 1 до 100. Спробуйте вгадати.")  # Виводимо інструкції для користувача

  while True:  # Запускаємо нескінченний цикл, який триває до тих пір, поки користувач не вгадає число
    try:  # Початок блоку try для обробки винятків
      guess = int(input("Ваша спроба: "))  # Запитуємо користувача ввести число та перетворюємо його на ціле число
      attempts += 1  # Збільшуємо кількість спроб на 1

      if guess < secret_number:  # Якщо вгадане число менше загаданого
        print("Загадане число більше.")  # Виводимо повідомлення, що загадане число більше
      elif guess > secret_number:  # Якщо вгадане число більше загаданого
        print("Загадане число менше.")  # Виводимо повідомлення, що загадане число менше
      else:  # Якщо вгадане число дорівнює загаданому
        print(f"Вітаю! Ви вгадали число {secret_number} з {attempts} спроб!")  # Виводимо повідомлення про перемогу
        break  # Виходимо з циклу

    except ValueError:  # Обробка винятку ValueError, який виникає, якщо користувач вводить не ціле число
      print("Будь ласка, введіть ціле число.")  # Виводимо повідомлення про помилку

if __name__ == "__main__":  # Перевіряємо, чи запускається скрипт як основна програма
  guess_the_number()  # Викликаємо функцію guess_the_number для запуску гри


4. Використання:
Запустіть скрипт Python.
Слідуйте інструкціям на екрані, вводячи свої спроби вгадати число.
Програма надаватиме підказки, допоки ви не вгадаєте число.
5. Структура програми:
import random: Імпортує модуль random, який використовується для генерації випадкових чисел.
guess_the_number(): Функція, що містить основну логіку гри.
Генерує випадкове число за допомогою random.randint(1, 100).
Ініціалізує лічильник спроб.
Запускає цикл while True, який триває до тих пір, поки користувач не вгадає число.
Обробляє введення користувача за допомогою try...except, щоб уникнути помилок, якщо користувач введе не ціле число.
Порівнює введене число з загаданим і виводить відповідні підказки.
Виводить повідомлення про перемогу, коли користувач вгадує число.
if __name__ == "__main__":: Перевіряє, чи запускається скрипт як основна програма, і викликає функцію guess_the_number().
6. Приклади використання:
Ласкаво просимо до гри 'Вгадай число'!
Я загадав число від 1 до 100. Спробуйте вгадати.
Ваша спроба: 50
Загадане число менше.
Ваша спроба: 25
Загадане число більше.
Ваша спроба: 37
Загадане число менше.
Ваша спроба: 31
Вітаю! Ви вгадали число 31 з 4 спроб!


7. Примітки:
Програма використовує цикл while True, який завершується тільки тоді, коли користувач вгадує число.
Використання try...except дозволяє обробляти помилки введення, коли користувач вводить не ціле число.













