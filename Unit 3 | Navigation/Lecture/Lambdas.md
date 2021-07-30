## [Lambda]

Then there is an arrow -> which is followed by the return type.


## [Crash Course on Kotlin](https://developer.android.com/codelabs/basic-android-kotlin-training-collections?continue=https%3A%2F%2Fdeveloper.android.com%2Fcourses%2Fpathways%2Fandroid-basics-kotlin-unit-3-pathway-1%23codelab-https%3A%2F%2Fdeveloper.android.com%2Fcodelabs%2Fbasic-android-kotlin-training-collections#1)



```
fun main() {
    val triple: (Int) -> Int = { a: Int -> a * 3 }
    println(triple(5))

    val triple: (Int) -> Int = { it * 3 }
     println(triple)
}
```

Output:

```
15
15
```


```
fun main() {
    val peopleNames = listOf("Fred", "Ann", "Barbara", "Joe")
    println(peopleNames.sorted())
    println(peopleNames.sortedWith { str1: String, str2: String -> str1.length - str2.length })
}
```

Output:

```
[Ann, Barbara, Fred, Joe]
[Ann, Joe, Fred, Barbara]
```
