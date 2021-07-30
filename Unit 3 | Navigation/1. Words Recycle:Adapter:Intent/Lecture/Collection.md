## [Collection]

A collection is a group of related items, like a list of words, or a set of employee records. The collection can have the items ordered or unordered, and the items can be unique or not. You've already learned about one type of collection, lists. Lists have an order to the items, but the items don't have to be unique.


## [Crash Course on Kotlin](https://developer.android.com/codelabs/basic-android-kotlin-training-collections?continue=https%3A%2F%2Fdeveloper.android.com%2Fcourses%2Fpathways%2Fandroid-basics-kotlin-unit-3-pathway-1%23codelab-https%3A%2F%2Fdeveloper.android.com%2Fcodelabs%2Fbasic-android-kotlin-training-collections#1)



```
fun main() {
    val numbers = listOf(0, 3, 8, 4, 0, 5, 5, 8, 9, 2)
    println("list:   ${numbers}")
    println("sorted: ${numbers.sorted()}")
    val setOfNumbers = numbers.toSet()
    println("set:    ${setOfNumbers}")
    val set1 = setOf(1,2,3)
    val set2 = mutableSetOf(3,2,1)
    println("$set1 == $set2: ${set1 == set2}")
    println("contains 7: ${setOfNumbers.contains(7)}")
}
```

Output:

```
list:   [0, 3, 8, 4, 0, 5, 5, 8, 9, 2]
sorted: [0, 0, 2, 3, 4, 5, 5, 8, 8, 9]
set:    [0, 3, 8, 4, 5, 9, 2]
[1, 2, 3] == [3, 2, 1]: true
contains 7: false
```
