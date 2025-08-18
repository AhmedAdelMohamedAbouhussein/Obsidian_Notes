![[Pasted image 20250818154101.png]]

## **2. Database Operations**

- **Create Database**: MongoDB creates database automatically when you insert data.
`use myDatabase`

- **Drop Database**: Deletes the database permanently.
`db.dropDatabase()`

---

## **3. Collection Operations**

- **Create Collection**
`db.createCollection("users")`

- **Show Collections**
`show collections`

- **Drop Collection**
`db.users.drop()`

---

## **4. Insert Documents**

- **Insert One Document**
`db.users.insertOne({   name: "Ahmed",   age: 22,   email: "ahmed@example.com" })`

- **Insert Many Documents**
`db.users.insertMany([   { name: "Ali", age: 25 },   { name: "Sara", age: 28 } ])`

---

## **5. Data Types**

MongoDB supports several BSON types:
`String, NumberInt, NumberLong, Double, Boolean, Date, ObjectId, Array, Embedded Document`

Examples:
`{ name: "Ahmed", age: 22, isActive: true, tags: ["student","developer"], createdAt: new Date() }`

---

## **6. Query Documents**

- **Find All Documents**
`db.users.find()`

- **Find with Query**
`db.users.find({ age: 22 })`

- **Projection (Select Fields)**
`db.users.find({ age: 22 }, { name: 1, email: 1, _id: 0 })`

- **Sort**
`db.users.find().sort({ age: -1 }) // -1 desc, 1 asc`

- **Limit**
`db.users.find().limit(2)`

---

## **7. Update Documents**

- **Update One**
`db.users.updateOne(   { name: "Ahmed" },    { $set: { age: 23 } } )`

- **Update Many**
`db.users.updateMany(   { age: { $lt: 25 } },    { $set: { isActive: true } } )`

- **Update Operators**
`$set, $inc, $rename, $unset, $push, $pull`

## **8. Comparison Operators**

|Operator|Example|Description|
|---|---|---|
|`$eq`|`{ age: { $eq: 22 } }`|Equal|
|`$ne`|`{ age: { $ne: 22 } }`|Not equal|
|`$gt`|`{ age: { $gt: 20 } }`|Greater than|
|`$gte`|`{ age: { $gte: 20 } }`|Greater or equal|
|`$lt`|`{ age: { $lt: 30 } }`|Less than|
|`$lte`|`{ age: { $lte: 30 } }`|Less or equal|
|`$in`|`{ age: { $in: [22,25,28] } }`|Matches any value in array|
|`$nin`|`{ age: { $nin: [22,25] } }`|Not in array|

---

## **9. Logical Operators**

|Operator|Example|Description|
|---|---|---|
|`$and`|`{ $and: [{ age: { $gt: 20 } }, { age: { $lt: 30 } }] }`|AND|
|`$or`|`{ $or: [{ age: 22 }, { age: 25 }] }`|OR|
|`$not`|`{ age: { $not: { $gt: 25 } } }`|NOT|
|`$nor`|`{ $nor: [{ age: 22 }, { age: 25 }] }`|NOR|

---

## **10. Delete Documents**

- **Delete One**
`db.users.deleteOne({ name: "Ahmed" })`

- **Delete Many**
`db.users.deleteMany({ age: { $lt: 25 } })`

---

## **11. Indexes**

- **Show Indexes**
`db.users.getIndexes()`

- **Create Index**
`db.users.createIndex({ email: 1 }) // 1 ascending, -1 descending`

- **Drop Index**
`db.users.dropIndex("email_1")`

---

## **12. Aggregation (Optional)**

- **Count Documents**
`db.users.countDocuments({ age: { $gt: 20 } })`

- **Distinct Values**
`db.users.distinct("age")`

---

## **13. Useful Tips**

- `_id` is auto-generated if not provided.
- MongoDB is **schema-less**, but you can define **validators**.
- Use **`pretty()`** for readable output:
`db.users.find().pretty()`