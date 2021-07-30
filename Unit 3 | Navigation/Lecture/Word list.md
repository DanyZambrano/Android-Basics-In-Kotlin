## [Word List]

## [Crash Course on Kotlin](https://developer.android.com/codelabs/basic-android-kotlin-training-collections?continue=https%3A%2F%2Fdeveloper.android.com%2Fcourses%2Fpathways%2Fandroid-basics-kotlin-unit-3-pathway-1%23codelab-https%3A%2F%2Fdeveloper.android.com%2Fcodelabs%2Fbasic-android-kotlin-training-collections#1)


The startsWith() function returns true if a string starts with the specified string. You can also tell it to ignore case, so "b" will match "b" or "B".

The shuffled() function to make a copy of a collection with the items randomly shuffled. Change the filtered words to be shuffled

The take() function to get the first items in the collection


```
fun main() {
    val words = listOf("about", "acute", "awesome", "balloon", "best", "brief", "class", "coffee", "creative")

    val filteredWords1 = words.filter { it.startsWith("b", ignoreCase = true) }
    println(filteredWords1)

    val filteredWords2 = words.filter { it.startsWith("b", ignoreCase = true) }
    .shuffled()
    println(filteredWords2)

    val filteredWords3 = words.filter { it.startsWith("b", ignoreCase = true) }
    .shuffled()
    .take(2)
    println(filteredWords3)

    val filteredWords4 = words.filter { it.startsWith("b", ignoreCase = true) }
    .shuffled()
    .take(2)
    .sorted()
    println(filteredWords4)
}
```

Output:

```
[balloon, best, brief]

[brief, balloon, best]

[brief, balloon]

[balloon, brief]
```

