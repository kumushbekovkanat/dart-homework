# dart-homework

void main() {
  print('Задание 1');
  int age = 17;
  bool isStudent = true;
  bool isBlocked = false;

  if (isBlocked) {
    print('Доступ запрещён');
  } else if (!isBlocked && age >= 18) {
    print('Доступ разрешён');
  } else if (age < 18 && isStudent) {
    print('Доступ разрешён для студента');
  } else {
    print('Доступ запрещён');
  }

  print('');
  print(' Задание 2');
  List<int> numbers = [12, 5, 8, 21, 16, 3, 10];

  print('Все элементы:');
  for (int i = 0; i < numbers.length; i++) {
    print(numbers[i]);
  }

  int sum = 0;
  int evenCount = 0;
  int oddCount = 0;
  int maxNumber = numbers[0];

  for (int number in numbers) {
    sum = sum + number;
    if (number % 2 == 0) {
      evenCount = evenCount + 1;
    } else {
      oddCount = oddCount + 1;
    }
    if (number > maxNumber) {
      maxNumber = number;
    }
  }

  print('Сумма: $sum');
  print('Чётных: $evenCount');
  print('Нечётных: $oddCount');

  print('Числа больше 10:');
  for (int number in numbers) {
    if (number > 10) {
      print(number);
    }
  }

  print('Самое большое число: $maxNumber');

  print('');
  print('Задание 3 ');
  List<int> grades = [85, 42, 90, 67, 55, 100, 38];

  int passed = 0;
  int failed = 0;
  int gradesSum = 0;

  for (int grade in grades) {
    gradesSum = gradesSum + grade;

    if (grade >= 90 && grade <= 100) {
      print('$grade - Отлично');
    } else if (grade >= 70 && grade <= 89) {
      print('$grade - Хорошо');
    } else if (grade >= 50 && grade <= 69) {
      print('$grade - Удовлетворительно');
    } else {
      print('$grade - Неудовлетворительно');
    }

    if (grade >= 50) {
      passed = passed + 1;
    } else {
      failed = failed + 1;
    }
  }

  double average = gradesSum / grades.length;

  print('Сдали экзамен: $passed');
  print('Не сдали экзамен: $failed');
  print('Средний балл: $average');

  if (average >= 70 && passed > failed) {
    print('Группа успешно сдала экзамен');
  } else {
    print('Результаты группы необходимо улучшить');
  }

  print('');
  print('Корзина покупок ');
  List<String> products = ['Хлеб', 'Молоко', 'Яйца'];
  List<int> prices = [40, 80, 120];

  int total = 0;

  for (int i = 0; i < products.length; i++) {
    print('${products[i]} - ${prices[i]} сом');
    total = total + prices[i];
  }

  print('Общая стоимость: $total сом');

  double finalPrice = total.toDouble();

  if (total > 500) {
    finalPrice = total * 0.8;
    print('Скидка 20%');
  } else if (total > 200) {
    finalPrice = total * 0.9;
    print('Скидка 10%');
  } else {
    print('Скидки нет');
  }

  print('Итоговая сумма: $finalPrice сом');
}
