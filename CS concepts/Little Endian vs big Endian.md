## 🔹 1. Big Endian

> The **most significant byte (MSB)** is stored **first** (at the lowest memory address).

🧩 Example:  
Suppose we want to store this 4-byte integer:

`0x12345678`

In **Big Endian** memory:

|Address|Stored Byte|
|---|---|
|1000|12|
|1001|34|
|1002|56|
|1003|78|

✅ **Human-friendly** — looks like the number we read.

---

## 🔹 2. Little Endian

> The **least significant byte (LSB)** is stored **first** (at the lowest memory address).

Same number:

`0x12345678`

In **Little Endian** memory:

|Address|Stored Byte|
|---|---|
|1000|78|
|1001|56|
|1002|34|
|1003|12|

✅ **Machine-efficient** — easier for CPUs to read increasing values.

---

## 🧩 Visual Comparison

|Representation|Memory Order (Low → High)|
|---|---|
|Big Endian|`12 34 56 78`|
|Little Endian|`78 56 34 12`|