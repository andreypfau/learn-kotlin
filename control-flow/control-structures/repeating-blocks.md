# Циклы

Иногда вам нужно повторить группу команд несколько раз. Вы можете просто скопировать это выражение.
Что, если вы захотите повторить это сто тысяч раз? Copy-Paste в этом случае не практичен.

К счастью, для нас, Kotlin предоставляет несколько специальных инструкций для многократного повторения блоков кода.
Эти операторы известны как **циклы**. Они полезны, когда дело доходит до повторения нескольких утверждений.

## Цикл повтора

Чтобы использовать простейший цикл,
напишите `repeat(n)` и последовательность команд в фигурных скобках `{...}`.
`n` - это целое число, которое определяет, сколько раз эти команды будут повторяться.

```kotlin
repeat(n) {
    // команды
}
```

Например, приведенная ниже программа выводит `Привет` три раза:

```kotlin
fun main() {
    repeat(3) {
        println("Привет")
    }
}
```

Вывод:

```
Привет
Привет
Привет
```

?> Если `n` равно нулю или отрицательному числу, Kotlin проигнорирует цикл. Если `n` равно единице, инструкции будут
выполняться только один раз.

## Чтение и обработка данных в цикле

Вы можете считывать данные из стандартного ввода,
объявлять переменные и даже выполнять вычисления внутри инструкции `repeat`.

Взгляните на этот пример. Приведенная ниже программа считывает числа из стандартного ввода и вычисляет их сумму.
Первое число не является частью суммы, оно определяет длину входной последовательности.

```kotlin
fun main() {
    val n = readln().toInt()
    var sum = 0

    repeat(n) {
        val next = readln().toInt()
        sum += next
    }

    println(sum)
}
```

Этот код считывает длину числовой последовательности и присваивает ее переменной `n`.
После этого он создаёт переменную для хранения общей суммы.
Код считывает следующее число и добавляет его к сумме ровно `n` раз.
Затем цикл останавливается, и программа выводит общую сумму.

Вот пример входных чисел:

```
5
40
15
30
25
50
```

Вывод:

```
160
```

## Заключение

Циклы полезны, когда вам нужно повторить оператор в вашем коде.
В этом разделе мы обсуждали цикл `repeat()`. Это очень простой инструмент.
Определите количество выполнений, затем оператор в фигурных скобках, и вперед!
На следующем уроке мы узнаем о продвинутых циклах и о том, как их можно применить к более сложным задачам.
