# Матричный калькулятор
Написать программу, которая вычисляет определитель, характеристический полином и обратную матрицу для квадратной матрицы (элементы матрицы – вещественные числа).

Выполняемое действие, имя файла с матрицей и имя файла для записи ответа задаются в командной строке. 
Например, для вычисления обратной матрицы, для матрицы, заданной в файле `input.txt`, и записи ответа в файл `output.txt`:
```
   ./matrixcalc -inv input.txt output.txt
```

Характеристический полином матрицы A: `det(lambda * E - A)`. Для вычисления характеристического полинома матрицы можно использовать [метод Леверье](http://vmath.ru/vf5/algebra2/charpoly#metod_levere) или [метод Крылова](http://vmath.ru/vf5/algebra2/charpoly#metod_krylova).

## Требования
Программа не должна использовать контейнеры STL (std::vector, std::string и т. д.). 

## Формат файлов
Формат файлов, в которых записаны входные матрицы и формат файла с матрицей, которая получается в результате вычисления, одинаковый:
* в первой строке файла указаны два целых числа через пробел: количество строк и количество столбцов матрицы;
* во второй строке и далее записаны элементы матрицы по строкам. 

## Вход
* первый аргумент командной строки – `-det` (для вычисления определителя), `-poly` (для вычисления характеристического полинома) или `-inv` (для вычисления обратной матрицы);
* второй аргумент командной строки – имя файла, в котором записана исходная матрица;
* третий аргумент командной строки – имя файла, в который будет записан результат. 

## Выход
При вычислении определителя в выходной файл необходимо записать одно число – определитель матрицы или `error`, если определитель не может быть вычислен.

При вычислении характеристического полинома в выходной файл необходимо записать матрицу (вектор-строку) с коэффициентами полинома или `error`, если характеристический полином не может быть вычислен.

Программа, вычисляющая обратную матрицу, должна записать в выходной файл:
* обратную матрицу,
* `singular`, если матрица вырожденная,
* `error`, если обратная матрица не может быть вычислена.

