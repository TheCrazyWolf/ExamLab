# Экзаменационная работа по прикладном программированию

``` csharp
// See https://aka.ms/new-console-template for more information
// Работа студента группы ИВТз-22у
// Кулагина Алексея Александровича

// Глубина массива 
var rows = 4;
var cols = 4; 

// Создаем массив с числами
var arrayNums = new int[rows,cols];

// Создание экземпляра класса Random
var random = new Random();

// Проходимся по массиву и заполняем его случайными числами от 0 до 15
for (var index = 0; index < rows; index++)
{
    for (var indexInArray = 0; indexInArray < cols; indexInArray++)
    {
        arrayNums[index, indexInArray] = random.Next(0, 15); 
    }
}

// Массив булевых значений
var arrayBooleans = new bool[rows, cols];

// Проходимся по массиву и заполняем его случайными true /false
for (var index = 0; index < rows; index++)
{
    for (var indexInArray = 0; indexInArray < cols; indexInArray++)
    {
        arrayBooleans[index, indexInArray] = Convert.ToBoolean(random.Next(0, 2));  // Генерируем 0 / 1 и конвертируем в bool
    }
}

// Итоговый результат
var totalSum = 0;

// Проходимся по массиву и считаем

for (var indexNum = 0; indexNum < arrayNums.GetLength(0); indexNum++)
{
    for (var indexBoll = 0; indexBoll < arrayNums.GetLength(1); indexBoll++)
    {
        if (arrayBooleans[indexNum, indexBoll])
            totalSum += arrayNums[indexNum, indexBoll];
    }
}

Console.WriteLine($"Result: {totalSum}");
```
