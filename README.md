Задача алгоритмически не самая сложная, однако для полноценного выполнения проверочной работы необходимо:

1. Создать репозиторий на GitHub
2. Нарисовать блок-схему алгоритма (можно обойтись блок-схемой основной содержательной части, если вы выделяете её в отдельный метод)
3. Снабдить репозиторий оформленным текстовым описанием решения (файл README.md)
4. Написать программу, решающую поставленную задачу
5. Использовать контроль версий в работе над этим небольшим проектом (не должно быть так, что всё залито одним коммитом, как минимум этапы 2, 3, и 4 должны быть расположены в разных коммитах)
## Задача: Написать программу, которая из имеющегося массива строк формирует новый массив из строк, длина которых меньше, либо равна 3 символам. Первоначальный массив можно ввести с клавиатуры, либо задать на старте выполнения алгоритма. При решении не рекомендуется пользоваться коллекциями, лучше обойтись исключительно массивами.

## Примеры:
## [“Hello”, “2”, “world”, “:-)”] → [“2”, “:-)”]
## [“1234”, “1567”, “-2”, “computer science”] → [“-2”]
## [“Russia”, “Denmark”, “Kazan”] → []

string[] array =  ["Russia", "Denmark", "Kazan"];  // строка с данными 
int count = 0;                                     // вводим начальное значение счетчика count
for (int i = 0; i < array.Length; i++)             // запускаем цикл 
{
   if(array[i].Length < 4)                         // задаём условие цикла
    {
       count++;                                    // счетчик с прибавлением +1
    } 
} 
string[] result = new string[count];               // вывод новой строки с полученными значениями счетчика

int j = 0;                                         // ввод переменной j
for (int i = 0; i < array.Length; i++)             // запускаем цикл с  ограничением кол-ва символов до 4х, т.е. 3
{
    if(array[i].Length<4)
    {
        result[j]=array[i];
        j++;
    }
}

for (int i = 0; i < result.Length; i++)             
{
   Console.Write($"{result[i]}\t");               // выполняя условие цикла выводим значение в консоль.
}