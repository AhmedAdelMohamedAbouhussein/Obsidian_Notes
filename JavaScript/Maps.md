## **1. What is a Map?**

A **`Map`** is a collection of key-value pairs where:

- Keys can be **any type** (strings, numbers, objects, functions, etc.)
- Keys maintain **insertion order**
- Unlike plain objects, Maps have a **size property**, and no prototype keys (`__proto__`) interfere.

![[Pasted image 20250828194939.png]]

## **2. Popular Map Methods**

### **2.1 `set(key, value)`**

Adds or updates a key-value pair.

`const map = new Map(); map.set("a", 1); map.set("b", 2); map.set("a", 3); // Updates value for key "a" console.log(map.get("a")); // 3`

---

### **2.2 `get(key)`**

Retrieves the value for a key.

`console.log(map.get("b")); // 2 console.log(map.get("c")); // undefined`

---

### **2.3 `has(key)`**

Checks if a key exists in the map.

`console.log(map.has("a")); // true console.log(map.has("z")); // false`

---

### **2.4 `delete(key)`**

Removes a key-value pair.

`map.delete("a"); console.log(map.has("a")); // false`

---

### **2.5 `clear()`**

Removes all entries.

`map.clear(); console.log(map.size); // 0`

---

### **2.6 `size`**

Number of entries in the map.

`console.log(map.size); // returns the count of key-value pairs`

---

### **2.7 `keys()`, `values()`, `entries()`**

These methods return **iterators** over keys, values, or `[key, value]` pairs.

`const map = new Map([["a", 1], ["b", 2]]);  console.log([...map.keys()]);   // ["a", "b"] console.log([...map.values()]); // [1, 2] console.log([...map.entries()]); // [["a", 1], ["b", 2]]`

- `entries()` is what we used in your React example to iterate `[platform, gamesMap]`.
    

---

### **2.8 `forEach(callback)`**

Iterates over all entries.

`map.forEach((value, key) => {   console.log(key, value); }); // Output: // a 1 // b 2`

---

### **2.9 `Array.from()` and Spread `[...map]`**

Convert Map to array for mapping/filtering.

`const arr = Array.from(map.entries()); // [["a", 1], ["b", 2]] const arr2 = [...map];                // same as above`

Turns any iterable (like `Map.entries()`) into an array:

`const mapArray = Array.from(map.entries()); // [["steam", {730: "CS2", 570: "Dota 2"}], ["xbox", {1234: "Halo"}]]`

- This lets you use array methods like `.map()` or `.flatMap()` on Maps.

---

### **2.10 `flatMap()`**

**Not a Map method**, but often used with Map converted to array:

`const map = new Map([   ["steam", {730: "CS2", 570: "Dota2"}],   ["xbox", {1234: "Halo"}] ]);  // Flatten nested object into array of games const gamesArray = Array.from(map.entries()).flatMap(([platform, gamesObj]) => {   return Object.entries(gamesObj).map(([id, name]) => ({     platform,     gameId: id,     gameName: name   })); });  console.log(gamesArray); /* [   { platform: "steam", gameId: "730", gameName: "CS2" },   { platform: "steam", gameId: "570", gameName: "Dota2" },   { platform: "xbox", gameId: "1234", gameName: "Halo" } ] */`


## **`Object.entries()`**

Converts an object into an array of `[key, value]` pairs:

`const steamGames = { 730: "CS2", 570: "Dota 2" }; Object.entries(steamGames); // [["730", "CS2"], ["570", "Dota 2"]]`

- Useful when you have a nested object **inside a Map** and want to iterate it like a Map.
