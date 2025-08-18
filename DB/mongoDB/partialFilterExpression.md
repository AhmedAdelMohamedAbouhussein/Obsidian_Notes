In **MongoDB**, the `partialFilterExpression` option is used when creating an **index** to specify a **filter condition** for which documents should be included in the index. Essentially, it makes the index **partial**, meaning only documents that match the filter are indexed. This can save space and improve performance when you don’t need every document to be in the index.

Suppose you have a `users` collection:
![[Pasted image 20250817140906.png]]

If you want a **unique index on `steamId`**, but allow multiple documents **without `steamId`**, you can use a partial filter:
![[Pasted image 20250817140932.png]]

