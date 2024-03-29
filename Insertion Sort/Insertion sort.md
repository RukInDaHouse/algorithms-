# Сортировка вставками
**Алгоритм сортировки;**  
**Временная сложность**: O(n²);  

Сортировка вставками — алгоритм сортировки, в котором элементы входной последовательности просматриваются по одному, и каждый новый поступивший элемент размещается в подходящее место среди ранее упорядоченных элементов. Этот алгоритм эффективно работает при сортировке небольшого количества элементов. 

Сортировка вставкой напоминает способ, которым игроки сортируют имеющиеся на руках карты. Пусть в левой руке нет карт, и все они лежат на столе, рубашкой вверх. Со стола берется по одной карте, каждая из которых помещается в нужное место среди карт в левой руке. Чтобы определить место очередной карты, ее достоинство сравнивается с достоинстовм других карт в руке. Таким образом, в любой момент времени карты будут рассортированы в левой руке.  

![Иллюстрация к алгоритму](https://miro.medium.com/max/1280/1*jdXtqXw0EQVpqdZZoGnwsQ.gif)

**Шаг 1:** Двигаясь слева направо, выберите каждую карту.  

**Шаг 2:** Переместите его в правильное положение среди других слева от него.  

**Шаг 3:** И так далее, пока не дойдете до конца.  

## Описание
Изначально отсортированная последовательность пуста. На вход алгоритма подаётся последовательность ***n*** чисел (также известных под названием ***ключи***) вида: ***a(1)***, ***a(2)***, ... ,***a(n)***. На выходе алгоритм должен вернуть перестановку исходной последовательности, чтобы выполнялось следующее свойство: ***a(1)*** <= ***a(2)*** <= ... , <= ***a(n)***.

![Иллюстрация к алгоритму](https://upload.wikimedia.org/wikipedia/commons/9/9c/Insertion-sort-example.gif)  

## Эффективность
Сортировка вставками наиболее эффективна при малом количестве элементов или при частично отсортированом массиве. Если же элементов меньше 10, то данный алгоритм является лучшим. Наихудший случай — когда элементы исходной последовательности расположены в обратном порядке.  

## Псевдокод
```
function insertionSort(a):
  for i = 1 to n - 1
    j = i - 1
    while j ⩾ 0 and a[j] > a[j + 1] 
      swap(a[j], a[j + 1]) //Функция swap меняет местами элементы a[j] и a[j + 1]
      j--
```