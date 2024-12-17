# Maps 🗺️

## Create a Mutable Map
- **`val map: MutableMap<Char, Int> = mutableMapOf()`** — Create a mutable map where the key is a `Char` and the value is an `Int`. 📝

## Default Value for Non-Existent Keys
- **`map[k] ?: 0`** — Use a default value (`0` in this case) if the key does not exist in the map. 🔑

## Check If a Key Exists
- **`map.containsKey(X)`** — Check if a specific key `X` exists in the map. ✔️

## Convert Map Values to a List
- **`map.values.toList()`** — Convert the values of the map to a list. 📋

## Modify Map to Add to a List of Values
- **`map.computeIfAbsent(root) { mutableListOf() }.add(email)`** — Modify the map by adding to a list of values for a given key. ✨

## Convert Map Values to a List (Another Approach)
- **`ret.values.toList()`** — Convert the values of a map to a list. 🔄