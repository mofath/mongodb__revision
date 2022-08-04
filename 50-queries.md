# Group
- $group is used to group document by specific field.   
- $group by null means all documents will be grouped into one.

```js 
db.collection.aggregate([{
	$group: {
		"_id": "$dept"
	}
}])

// result
[
  { "_id": "hr"},
  { "_id": "emp" },
  {"_id": "admin"}
]
```

# Sum
- $sum used to sum the values inside a group   

```js 
db.collection.aggregate([{
	$group: {
		"_id": "$dept",
		"noOfEmps": {
			$sum: 1
		}
	}
}])

// result
[
  { "_id": "hr"},
  { "_id": "emp" },
  {"_id": "admin"}
]
```