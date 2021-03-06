# MysteriousPyramid.
Треугольник четных чисел.


![Image](scrin01.png)


  Рассмотрим треугольник четных чисел. Кому удобно оперировать табличными понятиями можно рассматривать как таблицу.
  
Алгоритм заполнения треугольника:
 - числовой ряд четных чисел;
 - первая строка или вершина треугольника является первый член последовательности;
 - каждая следующая строка состоит из очередных элементов четной последовательности;
 - в каждой строке количество элементов равно номеру этой строки;



                   0                                              2
                 2   4                                          4   6
               6   8   10                                      8  10  12
             12  14  16   18                                14  16  18  20
          20  22  24  26   28                            22  24  26  28  30
         30  32  34  36  38  40           или           32  34  36  38  40  42



  Вершиной пирамиды является первый член четной последовательности, 
а так как четная последовательность начинается с числа "2" ... или с числа "0", 
не будем спорить кто прав, стороники которые считают что ноль это четное число,
или стороники которые за то что ноль это нечетное или те кто за то что это нейтральное число, 
или бичетное т.е. и четное и нечетное одновремено.
  
  Я на всякий случай иследовал оба варианта.
  
  В виде таблицы  
  
  | шаг | четные числа             | сумма  |                     
  |-----|:------------------------:|-------:|                     
  |  1  | 0                        |    0   |                     
  |  2  | 2   4                    |    6   |                     
  |  3  | 6   8   10               |   24   |                     
  |  4  | 12  14  16  18           |   60   |                     
  |  5  | 20  22  24  26  28       |  120   |                     
  |  6  | 30  32  34  36  38  40   |  210   |              
  
  
  или    
  
  
  | шаг | четные числа             | сумма  |
  |-----|:------------------------:|-------:|
  |  1  | 2                        |    2   |
  |  2  | 4   6                    |   10   |
  |  3  | 8   10  12               |   30   |
  |  4  | 14  16  18  20           |   68   |
  |  5  | 22  24  26  28  30       |  130   |
  |  6  | 32  34  36  38  40  42   |  222   |
  
  
   Формула для получения суммы на n-ом шаге :
                                  
                 Z = n^3 - n                                                     Z = n^3 + n
                 
  Я думаю тут даже коментировать или что то объяснять излишне.
  т.е. сумма n-ой строки равна куб номера этой строки минус номер этой же строки.
  
  
  Также можно обратить внимание на вторую закономерность:
    
  первое число в каждой строке равно произведению номера этой строки на номер предыдущей строки
  
                 A1 = n * n-1                                                    A1 = (n * (n-1)) + 2
                 
    
  Проверка числа.
  
  Например:
   
     Задано целое не отрицательное число X от 0 до 100000000.
    Проверить принадлежит ли это число треугольнику, т.е. является ли число X суммой какой то строки,
    проверять оба варианта треугольника,
    если принадлежит то определить номер строки и все элементы этой строки
    
    
  Теперь все выше сказанное попытаемься изложить в виде кода, для удобства JS и HTML\CSS будет у меня в одном файле.
  
Пригодится тем кто составляет листы собеседований, задачнки и т.д т.п.




 
  
