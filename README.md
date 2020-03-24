[![Build Status](https://travis-ci.com/Grishameister/APO_11_C_CPP_HW.svg?branch=making-hw-2)](https://travis-ci.com/Grishameister/APO_11_C_CPP_HW)
[![Coverage Status](https://coveralls.io/repos/github/Grishameister/APO_11_C_CPP_HW/badge.svg?branch=making-hw-2)](https://coveralls.io/github/Grishameister/APO_11_C_CPP_HW?branch=making-hw-2)

Выполнил Григорий Ролдугин, группа АПО-11.

Условие ИЗ №2:
Сравните и выведите в консоль время работы последовательного и параллельного с использованием нескольких процессов алгоритмов, каждый из которых выделяет в динамической памяти символьный массив размером 100 Мб и выполняет поиск в тексте максимальной последовательности, заключенной между символами кавычек и начинающейся с буквы латинского алфавита в верхнем регистре

Комментарии к работе:
Реализованы 2 библиотеки, собираются в зависимости от cmake команды ENABLE_PARALLEL. Так же стресс-тест на основе того, что пишем результат одной библиотеки в файл с помощью write_test.c, пересобираем, и сравниваем результат с другой в функции read_test.c
Вывод по реализации и алгоритму:последовательная реализация быстрее, так как в моей параллельной реализации используются записи в каналы, которые являются блокирующими операциями.
