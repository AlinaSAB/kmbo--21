# Домашние задания для КМБО-03-21, КМБО-04-21 и КМБО-06-21

Первоначальная настройка и особенности работы в различных средах разработки описаны в [Wiki](../../wiki).

UML-диаграммы (файлы с расширением `.xmi`) можно обрабатывать в программе [Umbrello](https://umbrello.kde.org/).

## Животные №1

1. Создать иерархию классов, описывающих классификацию животных:
   * 3 уровня (например: `Animal` - `Mammal` - `Cat`), на первом уровне `class Animal`.
   * Минимум два дочерних класса для каждого родительского класса.
   * В каждом классе создать одно публично (`public`) доступное поле, отражающее уникальность соответствующего таксона.
     Например, для класса `Cat` это может быть (средняя) длина вибриссов: `float vibrissaLength`.

2. Создать в `main()` по 1 объекту каждого класса нижнего уровня и установить разумные значения для всех доступных полей в данных объектах.

3. По образу и подобию кода в `vehicles.h` и `vehicles.cpp`:
   1. Добавить функцию `about()`.
   2. Реализовать оператор вывода в поток для `Animal`.

## Животные №2

1. Сделать все поля приватными, а доступ к ним сделать через пару методов («геттер» и «сеттер»), например:
```cpp
    private:
        int foo;
    public:
        int  getFoo() const       { return foo; }
        void setFoo(int newValue) { foo = newValue; }
```
2. Реализовать конструкторы для всех классов, позволяющие инициализировать все поля каждого класса.
   Конструкторы родительских классов должны быть объявлены в области видимости `protected`.
