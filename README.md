# Binary Tree
## Бинарное дерево

#### _**Типы хранимых данных**_ – целочисленные и комплексные числа, класс Person

## **Операции над дервеом:**
- Map (построить новое дерево поэлементным преобразованием);
- Where (построить новое дерево, в которое входят лишь те узлы исходного, которые удовлетворяют заданному условию);
- Merge (Слияние);
- Извлечение поддерева (по заданному элементу);
- Поиск на вхождение поддерева;
- Поиск элемента на вхождение;
- Бинарное дерево - это структура данных, в которой каждый узел имеет не более двух потомков (детей), при чем каждый левый потомок меньше потомка, а каждый правый потомок больше потомка.

## **«Пользовательский интерфейс»**

**Программа предлагает:**
1. Выбрать тип данных
2. Провести тест
3. Узнать о программе
4. Выйти из программы

Нужно будет ввести количество элементов в дереве
Затем поэлементно заполняется дерево (первый элемент считается корнем дерева)
Программа предложит ввести операцию, которую хотите провести.

## **«Программный интерфейс»**

Реализован класс Tree, в него инкапсулирован класс List*.
Класс List имеет поля: 
- **value** - хранит значение элемента дерева
- **left*** и **right*** - указатели на соответствующие потомки дерева.

Реализованы классы: 
- Complex
- Person

Класс Complex представляет концепцию комплексных чисел. Поля int real, int imaginary представляют собой действительные и мнимые части комплексного числа. Также в этом классе была реализована перегрузка операторов.

Класс Tree представляет бинарное дерево. Поле root хранит указатель на корень дерева.

Полиморфизм реализован с помощью шаблонов.

## **«Тестирование»**

**Функции:**

 1. bool testMapInt()
 2. bool testWhereInt() 
 3. bool testMergeInt()
 4. bool testMapCmplx()
 5. bool testWhereCmplx()
 6. bool testMergeCmplx()
 7. bool testMapPerson()
 8. bool testWherePerson()
 9. bool testMergePerson()
 10. void AllTests()

- **(1-3)** - тесты на соответствующие функции для целых чисел
- **(4-6)** - тесты на соответствующие функции для комплексных чисел
- **(7-9)** - тесты на соответствующие функции для класса Person
 
  **По окончании, все тесты возвращают True или False**
 
- **(10)** – функция, объединяющая все функции тестирования (1-11); Осведомляет об удачном или провальном прохождении теста

**Реализуемые функции и операции класса List:**

- void freeTree(List** list) - Удаляет дерево
- void add(T value, List** tmp) - Добавляет элемент к дереву
- void Print(std::string &byPass) - Выводит дерево
- void map(function<T(T)> f, List \*list, Tree &b) - реализация функции map (возведение в квадрат)
- void where(function<bool(T)> f,List \*list, Tree &b) - реализация функции where (создает новое дерево, элементы которого удовлетворяют заданному условию)
- void void merge(List \*\*list1, List \*\*list2) - Слияние двух деревьев
- void extraction(tree&, T) - Извлечение поддерева по элементу
- bool searchElement(T data, List \*\*list) - Поиск элемента в дереве
- bool equalityTree(List \*\*list1, List \*\*list2) - Равенство деревьев (данная функция понадобилась для тестирования)
