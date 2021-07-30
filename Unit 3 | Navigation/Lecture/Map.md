## [Map]

The last type of collection you'll learn about in this codelab is a map or dictionary. A map is a set of key-value pairs, designed to make it easy to look up a value given a particular key. Keys are unique, and each key maps to exactly one value, but the values can have duplicates. Values in a map can be strings, numbers, or objects—even another collection like a list or a set.

The map() function (which shouldn't be confused with a map or dictionary collection above) applies a transformation to each item in a collection.


## [Crash Course on Kotlin](https://developer.android.com/codelabs/basic-android-kotlin-training-collections?continue=https%3A%2F%2Fdeveloper.android.com%2Fcourses%2Fpathways%2Fandroid-basics-kotlin-unit-3-pathway-1%23codelab-https%3A%2F%2Fdeveloper.android.com%2Fcodelabs%2Fbasic-android-kotlin-training-collections#1)



```
fun main() {
    val peopleAges = mutableMapOf<String, Int>(
        "Fred" to 30,
        "Ann" to 23
    )
    peopleAges.put("Barbara", 42)
    peopleAges["Joe"] = 51

    println(peopleAges)
    peopleAges.forEach { print("${it.key} is ${it.value}, ") }
    println(peopleAges.map { "${it.key} is ${it.value}" }.joinToString(", ") )

    val filteredNames = peopleAges.filter { it.key.length < 4 }
    println(filteredNames)
}
```

Output:

```
{Fred=30, Ann=23, Barbara=42, Joe=51}

Fred is 30, Ann is 23, Barbara is 42, Joe is 51,

Fred is 31, Ann is 23, Barbara is 42, Joe is 51

{Ann=23, Joe=51}
```

