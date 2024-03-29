# Лабораторная работа №1
# Ввод/вывод данных и арифметические операции

Для ввода/вывода данных используются потоки `cout` и `cin`. Первый расшифровывается как `console output`, т.е. вывод на консоль, второй - `console input`, т.е. ввод с консоли.

Рассмотрим самый простой пример кода на языке программирования c++:
```
#include <iostream>
using namespace std;

int main() {
    cout << "Hello, world!";
    return 0;
}
```
В первой строке мы подключаем библиотеку `iostream`, которая расшифровывается как `input/output stream`, т.е. поток ввода/вывода. Именно в ней находятся потоки `cout` и `cin`.

Вторая строка говорит о том, что мы будем использовать стандартное пространство имен. Если не написать эту строчку, то потоки `cout` и `cin` придется использовать следующим образом: `std::cout` и `std::cin`.

Третья строка `int main()` объявляет функцию с именем `main`, которая не принимает параметров и вовзращает значения типа `int`. После объявления функции ставится открывающая фигурная скобка, которая определяет тело функции до закрывающей фигурной скобки. Функция `main()` является точкой входа в программу, т.е. это самая первая функция, которая будет вызвана при работе программы. Если мы не определим функцию `main()`, то программа не сможет запуститься.

Четвертая строка `cout << "Hello, world!";` выводит строку `Hello, world!` на консоль. Мы как бы помещаем строку в поток вывода `cout`, используя `<<`. 

Пятая строка `return 0;` означает `вернуть 0`. Функция выполняется, пока не встретит ключевое слово `return`. В данном случае мы возвращаем целое число 0, что означает, что программа завершилась без ошибок.

На последней строке мы ставим закрывающую скобку, дабы показать, что тело функции закончено.

Обратите внимание, что в языке программирования c++ необходимо ставить `;` в конце каждой строки, кроме случаев, когда строка заканчивается на `{` или `}` и в строках с подключением библиотек.

## Объявление переменных

Объявление переменных в языке программирования c++ происходит следующим образом:
```
// тип_данных имя_переменной;
// пример
int a;
int b;
```

Переменные с одним типом данных можно объявлять в одной строке, перечисляя имена через запятую:

```
// тип_данных имя_переменной1, имя_переменной2, ..., имя_переменнойN ;
int a, b, c;
```

Затем объявленной переменной можно присвоить значение:
```
a = 2;
b = 5943;
```

Присвоить значение переменной можно сразу после объявления:
```
// тип_данных имя_переменной = значение;
int a = 24;
int b = 9332;
```

Если объявлена переменная `a` с типом данных `int`, то мы не сможем переопределить ее, а так же не сможем поместить в нее значение другого типа:

```
int a;
float a; // ошибка
a = "Hello, world!"; // ошибка
```

## Ввод чисел с консоли и запись их в переменные

Для того, чтобы считать данные с консоли (путем ввода с клавиатуры), используется поток `cin`:

```
#include <iostream>
using namespace std;

int main() {
    int a;
    cin >> a;
    cout << a;
    return 0;
}
```

Рассмотрим строку `cin >> a;`. Она означает, что мы помещаем значение из потока ввода `cin` в переменную с именем `a`, используя `>>`. Если вы ввели с клавиатуры значение `42`, то в переменной `a` будет помещено значение `42`. 

Затем мы выводим значение переменной `a` в консоль через `cout`, и на консоль будет выведено значение, которое мы ввели с клавиатуры.

## Ввод и вывод нескольких значений

```
#include <iostream>
using namespace std;

int main() {
    int a, b;
    cout << "Input your numbers: ";
    cin >> a >> b;
    cout << "Your numbers are: " << a << " and " << b;
    return 0;
}
```
Строка `cin >> a >> b;` означает, что мы ожидаем на вводе с консоли два числа. Они могут быть разделены пробелом или переносом строки через нажатие клавиши `enter`.

Рассмотрим строку `cout << "Your numbers are: " << a << " and " << b;`. Сначала на консоль выведется фраза `Your numbers are: `, затем значение переменной `a`, затем фраза ` and `, ну и наконец значение переменной `a`. Как мы видим, в поток вывода `cout` можно выводить значения разных типов: в нашем случае значения целого типа и строки. 

Обратите внимание, что `<<` не ставит пробелы между выводимыми значениями, поэтому значения могут "слипнуться". Чтобы этого избежать, между выводимыми значениями мы выводим строку, в которой уже стоят пробелы.

## Математические операции с целыми числами

С переменными типа данных `int` можно использовать математические операторы, такие же, как и в обычной математике:
```
#include <iostream>
using namespace std;

int main() {
    int x, y, z;
    x = 3;
    y = 9;
    z = x + y; // Сложение, результат: 12
    z = x - y; // Вычитание, результат: -6
    z = x * y; // Умножение, результат: 18
    z = x / y; // Целочисленное деление, результат: 0
    x = 10;
    y = 3;
    z = y / x; // Целочисленное деление, результат: 3
    z = y % x; // Деление с остатком, результат: 1

    return 0;
}
```

## Комментарии

Комментарии могут быть однострочными и многострочными. Однострочный комментарий начинается с двух прямых косых черт (слэшэй `//`). Пример однострочных комментариев виден на примере выше. Все, что написано в комментарии, не будет выполнено в программе.

Многострочный комментарий начинается с `/*` и заканчивается на `*/`.

```
// Привет, я однострочный комментарий.
/*
    Привет, я многострочный комментарий.
    Я могу занимать
    сколько угодно строчек
*/
```

## Перенос каретки на новую строку

При вводе данных с консоли или выводе данных на консоль переноса каретки на новую строку не происходит автоматически. Для этого можно использовать специальный символ `"\n"` или специальную переменную `endl`. Символ `"\n"` можно использовать внутри строки, `endl` можно использовать только как отдельную переменную. Специальная переменная `endl` находится в пространстве имен `std`, если мы не используем `using namespace std;`, то необходимо писать `std::endl`.

```
#include <iostream>
using namespace std;

int main() {
    int x, y, z;
    cout << "Enter the number:" << endl;
    cout << "Enter the number:\n";

    return 0;
}
```
Вывод данных будет идентичным.

## Оформление кода
Программы нужно писать красиво, иначе их будет неудобно читать. На реальной работе программы много раз читаются и переписываются другими людьми, поэтому соблюдать правила оформления кода очень важно. Если в общем, то главное правило — «делайте как в образце». Если конкретно:

1. После открывающейся фигурной скобки добавляется отступ (tab или 4 пробела) в начале строки, на строке с закрывающейся фигурной скобкой отступ убирается.

2. Все бинарные операции (+,−, *, /, %, =, <<, >>) окружаются пробелами.

3. После унарного минуса пробел не ставится (−5 нужно писать слитно).

4. Перед знаками препинания (запятая и точка с запятой) пробел не ставится, после — ставится.

5. После открывающейся и перед закрывающейся круглой скобкой пробел не ставится.

# Задание на лабораторную работу №1

## Как решать задачи:

Задача состоит из 3х частей: текст задачи, формат входных данных и формат выходных данных. Формат входных данных показывает, что подается на вход программе, а формат выходных данных - что должно быть выведено в результате работы программы.

В каждой задаче (кроме задачи на нахождение значения функции) имеются примеры, в соответствии с которыми вы должны выводить данные. Обратите внимание, что примеры необходимы только для того, чтобы вы убедились, что ваша программа работает правильно. При сдаче лабораторной работы ваш код будет помещен в автоматическую систему тестирования, в которой ваша программа будет проверяться с различными входными данными. 

Если в формате входных данных написано, что на вход подается одно целое число, это значит, что вы должны создать под нее переменную и использовать ее в расчетах. Не нужно жестко задавать переменным значения из примеров, и уж тем более не нужно жестко задавать результат работы программы, как в примере. Ваша программа должна работать с любыми поступаемыми данными в соответствие с форматом входных данных.

## 1. Три последовательных числа

Напишите программу вывода на экран трех последовательно идущих чисел, каждое на отдельной строке. Первое число вводит пользователь, остальные числа вычисляются в программе.

## Формат входных данных
На вход программе подается одно целое число.

## Формат выходных данных
Программа должна вывести три последовательно идущих числа на новой строке в соответствии с примером.

| Входные данные | Результат|
|:---:|:---:|
|7  |8 <br> 9 <br> 10|
|0  |1 <br> 2 <br> 3|
|-15  |-14 <br> -13 <br> -12|

## 2. Сумма трёх чисел
Напишите программу, которая считывает три целых числа и выводит на экран их сумму. Каждое число записано в отдельной строке.

## Формат входных данных
На вход программе подаётся три целых числа, каждое на отдельной строке.

## Формат выходных данных
Программа должна вывести сумму введенных чисел.

| Входные данные | Результат|
|:---:|:---:|
|1 <br> 2 <br> 3| 6 |
|1 <br> -1 <br> 10| 10 |
|133 <br> 566 <br> -49| 650 |

## 3. Куб

Напишите программу, вычисляющую объём куба и площадь его полной поверхности по введённому значению длины ребра.

## Формат входных данных
На вход программе подается одно целое число – длина ребра.

## Формат выходных данных
Программа должна вывести текст и числа в соответствии с примером.

*Примечание*. Обратите внимание, что на текущем этапе обучения мы не знаем про оператор возведения в степень, поэтому пользуемся определением степени числа – число умножается само на себя указанное количество раз.

| Входные данные | Результат|
|:---:|:---:|
|25| Volume: 15625 <br> Total area: 3750|
|56| Volume: 175616 <br> Total area: 18816 |
|7| Volume: 343 <br> Total area: 294|

## 4. Арифметические операции

Напишите программу, в которой вычисляется сумма, разность и произведение двух целых чисел, введенных с клавиатуры.

## Формат входных данных
На вход программе подаётся два целых числа, каждое на отдельной строке.

## Формат выходных данных
Программа должна вывести сумму, разность и произведение введённых чисел по примеру, каждое на отдельной строке.

| Входные данные | Результат|
|:---:|:---:|
|1 <br> 2| 1 + 2 = 3 <br> 1 - 2 = -1 <br> 1 * 2 = 1|
|10 <br> 10| 10 + 10 = 20 <br> 10 - 10 = 0 <br> 10 * 10 = 100 |
|6 <br> 3| 6 + 3 = 9 <br> 6 - 3 = 3 <br> 6 * 3 = 18 |

## 5. Четырехзначное число

Напишите программу для нахождения цифр четырёхзначного числа.

## Формат входных данных
На вход программе подаётся положительное четырёхзначное целое число.

## Формат выходных данных
Программа должна вывести текст в соответствии с примером.

| Входные данные | Результат|
|:---:|:---:|
|3281| Digit in thousands: 3 <br> Digit in hundreds: 2 <br> Digit in tens: 8 <br> Digit in ones: 1|
|1000| Digit in thousands: 1 <br> Digit in hundreds: 0 <br> Digit in tens: 0 <br> Digit in ones: 0|
|9999| Digit in thousands: 9 <br> Digit in hundreds: 9 <br> Digit in tens: 9 <br> Digit in ones: 9|

## 6. Значение функции (по вариантам)
Напишите программу, вычисляющую значение заданной в варианте функции. Вариант выбирается по порядку следования в списке учащихся. 

## Формат входных данных
На вход программе подается один, два или три целых числа в соответствии с вариантом.

## Формат выходных данных
Программа должна вывести значение заданной в варианте функции

| Вариант | Функция |
| :-----: | :-----: |
| 1, 11, 21 | $f(x, z) = 0.25x + 0.75z^2 + 1.5$|
| 2, 12, 22 | $f(x, z) = 0.75x^2 + 2.5z - 4$|
| 3, 13, 23 | $f(x) = 8x^3  + 10x^2 - 40$|
| 4, 14, 24 | $f(x, z, w) = 0.6x + 0.9z - 1.5w + 1.2$|
| 5, 15, 25 | $f(x, z) = -0.7x - 0.6z + 2.3$|
| 6, 16, 26 | $f(x, z) = -7x - 7z + 12$|
| 7, 17, 27 | $f(x) = -2x - 4x^2 + 3$|
| 8, 18, 28 | $f(x) = x^3 + 30x - 100$|
| 9, 19, 29 | $f(x, z, w) = -0.7x - 0.6z + 2.3w - 20$|
| 10, 20, 30 | $f(x) = 0.4x^3 + 0.2x^2 - 0.5$|

