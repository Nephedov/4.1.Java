# Домашнее задание к занятию «Testability, автотесты, введение в ООП: объекты и методы»

## Решения
#### Задание 1:
* <a href="https://github.com/Nephedov/4.1.Java/blob/main/src/BonusMilesService.java">BonusMilesService.java</a> - класс с методом расчета миль.
* <a href="https://github.com/Nephedov/4.1.Java/blob/main/src/Main.java">Main.java</a> - использование класса
  <a href="https://github.com/Nephedov/4.1.Java/blob/main/src/BonusMilesService.java">BonusMilesService.java</a>.

<a href="https://github.com/Nephedov/4.1.Java/tree/main">Репозиторий</a> c решением.
#### Задание 2:
* <a href="https://github.com/Nephedov/4.2.Java/blob/main/src/BmiDescription.java">BmiDescription.java</a> - класс с методом описания на основе индекса массы тела.
* <a href="https://github.com/Nephedov/4.2.Java/blob/main/src/BmiService.java">BmiService.java</a> - класс с методом расчета индекса массы тела.
* <a href="https://github.com/Nephedov/4.2.Java/blob/main/src/Main.java">Main.java</a> - использование классов
  <a href="https://github.com/Nephedov/4.2.Java/blob/main/src/BmiDescription.java">BmiDescription.java</a> и
  <a href="https://github.com/Nephedov/4.2.Java/blob/main/src/BmiService.java">BmiService.java</a>

<a href="https://github.com/Nephedov/4.2.Java/tree/main">Репозиторий</a> c решением.
#### Задание 3:
* <a href="https://github.com/Nephedov/4.3.Java/blob/main/src/CalcCredit.java">CalcCredit.java</a> - класс с методом расчета ежемесячного (аннуитетного) платежа.
* <a href="https://github.com/Nephedov/4.3.Java/blob/main/src/Main.java">Main.java</a> - использование класса
  <a href="https://github.com/Nephedov/4.3.Java/blob/main/src/CalcCredit.java">CalcCredit.java</a>.

<a href="https://github.com/Nephedov/4.3.Java/tree/main">Репозиторий</a> c решением.
## Что было сделано
### Задание 1
* Реализованы классы <a href="https://github.com/Nephedov/4.1.Java/blob/main/src/BonusMilesService.java">BonusMilesService.java</a> с методом расчета количества миль и продемонстрирована работа в
  <a href="https://github.com/Nephedov/4.1.Java/blob/main/src/Main.java">Main.java</a>.
### Задание 2
* Реализованы классы и продемонстрировано использование в <a href="https://github.com/Nephedov/4.2.Java/blob/main/src/Main.java">Main.java</a>:
  * <a href="https://github.com/Nephedov/4.2.Java/blob/main/src/BmiService.java">BmiService.java</a> - класс с методом расчета индекса массы тела.
  * <a href="https://github.com/Nephedov/4.2.Java/blob/main/src/BmiDescription.java">BmiDescription.java</a> - класс с методом описания на основе индекса массы тела.
### Задание 3
* Реализован класс <a href="https://github.com/Nephedov/4.3.Java/blob/main/src/CalcCredit.java">CalcCredit.java</a> с методом расчета ежемесячного (аннуитетного) платежа и продемонстрирована работа в
  <a href="https://github.com/Nephedov/4.3.Java/blob/main/src/Main.java">Main.java</a>.
  
## Задание 1. Мили — модернизация (обязательное к выполнению)

Вам необходимо модернизировать [приложение для расчёта миль](./PRIMITIVES.md). Теперь сама логика расчёта будет находиться в специально выделенном классе сервиса, а в Main мы будем лишь создавать объект этого сервиса и вызывать его метод, передавая аргументами все необходимые данные для расчёта. Получив от вызова метода рассчитанный результат, мы выведем его на экран.

#### Этапы выполнения
1. Создайте класс `BonusMilesService` (`File -> New -> Java Class`, вводите название и нажимаете `Enter`).
1. Определите в нём метод `calculate`, который:
    1. принимает на вход один параметр: `cost` типа `int`;
    1. анализируя значение переданного параметра, возвращает рассчитанное количество миль (тип — `int`).
    
Разместите следующий код в классе `Main`:

```java
public class Main {
    public static void main(String[] args) {
        BonusMilesService service = new BonusMilesService();
        int price = 10_000;
        int miles = service.calculate(price);
        System.out.println(miles);
    }
}
```

## Задание 2*. Индекс массы тела (необязательная задача)

#### Этапы выполнения
1. Собрать информацию о том, какие входные данные нужны для расчёта.
1. Создать класс `BmiService` с методом `calculate`.
1. Продемонстрировать в `Main` по аналогии с первой задачей:
    1. создание объекта,
    1. вызов метода `calculate`,
    1. печать в консоль результата,
  
## Задание 3*. Кредитный калькулятор (необязательная задача повышенной сложности)

Вам нужно провести небольшой анализ и написать свой `CreditPaymentService`, который умеет рассчитывать ежемесячный платёж (см. аннуитетный платёж).

Параметры, их количество, типы, а также формулу вам необходимо определить исходя из скриншотов ниже.

Обратите внимание: на тех же данных ваш сервис должен считать так же.

Чтобы это продемонстрировать, в `Main` создайте объект и три раза вызовите его метод `calculate`. Результаты каждого вызова выводите в консоль.

Скриншоты для решения задачи. Важно: это не реальный сервис.

![image](https://user-images.githubusercontent.com/53707586/145564347-174ef746-013e-4793-bda1-79d81ac18e65.png)
![image](https://user-images.githubusercontent.com/53707586/145564368-0c1aaa9c-563b-4177-9ad6-a9f9adef8f92.png)
![image](https://user-images.githubusercontent.com/53707586/145564380-5140f2ab-312c-46c1-b423-1e5c209617b5.png)
