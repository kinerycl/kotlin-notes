# Maps 🗺️

## Create a Mutable Map
- **`val map: MutableMap<Char, Int> = mutableMapOf()`** — Create a mutable map where the key is a `Char` and the value is an `Int`. 📝

## Create a Map with Initial Data
- **`val map = mapOf("key1" to "value1", "key2" to "value2")`** — Create an immutable map with key-value pairs. You can use the `to` keyword to associate keys with values. 🔑

## Default Value for Non-Existent Keys
- **`map[k] ?: 0`** — Use a default value (`0` in this case) if the key does not exist in the map. 🔑
    ```kotlin
    val map = mutableMapOf("a" to 1, "b" to 2)
    val result = map["c"] ?: 0 // returns 0 because "c" is not in the map
     ```

## Check If a Key Exists
- **`map.containsKey(X)`** — Check if a specific key `X` exists in the map. ✔️
    ```kotlin
    val map = mutableMapOf("a" to 1, "b" to 2)
    val exists = map.containsKey("a") // returns true
    ```

## Convert Map Values to a List
- **`map.values.toList()`** — Convert the values of the map to a list. 📋
    ```kotlin
    val map = mutableMapOf("a" to 1, "b" to 2)
    val valuesList = map.values.toList() // [1, 2]
    ```
## Convert Map Values to a List (Another Approach)
- **`ret.values.toList()`** — Convert the values of a map to a list. 🔄

## Modify Map to Add to a List of Values
- **`map.computeIfAbsent(root) { mutableListOf() }.add(email)`** — Modify the map by adding to a list of values for a given key. ✨
    ```kotlin
    val map = mutableMapOf<String, MutableList<String>>()
    map.computeIfAbsent("root") { mutableListOf() }.add("email@example.com")
    println(map) // {"root" to ["email@example.com"]}
    ```
## Populate a Map Quickly with Data
- Using associate to create a map from a list of pairs:
    ```kotlin
    val keys = listOf("a", "b", "c")
    val values = listOf(1, 2, 3)
    val map = keys.zip(values).toMap() // {"a" to 1, "b" to 2, "c" to 3}
    ```
## Why map.computeIfAbsent(char) { 0 } + 1 Does Not Save to the Map
- Explanation: The expression map.computeIfAbsent(char) { 0 } + 1 computes a value but does not save it back to the map. The computeIfAbsent method only adds the result to the map if the key is not already present, but the value is not modified or reassigned back to the map.  
    ```kotlin
    val map = mutableMapOf("a" to 1)
    map.computeIfAbsent("a") { 0 } + 1 // This does not update the map.
    println(map) // {"a" to 1}  
    ```

- To update the map, you would need to assign the result back:
    ```kotlin
    map["a"] = (map["a"] ?: 0) + 1
    println(map) // {"a" to 2}
    ```

## Safe Ways to Add to Map
- ```map[char] = (map[char] ?: 0) + 1``` — Safe way to add a value to the map. If the key is not found, it defaults to 0 before adding 1.
    ```kotlin
    val map = mutableMapOf("a" to 1)
    val char = "b"
    map[char] = (map[char] ?: 0) + 1 // Adds 1 to "b"
    println(map) // {"a" to 1, "b" to 1}
    ```

## Clear All Elements in a Map
- map.clear() — Removes all entries from the map.
    ```kotlin
    val map = mutableMapOf("a" to 1, "b" to 2)
    map.clear() // Removes all entries
    println(map) // {}
    ```