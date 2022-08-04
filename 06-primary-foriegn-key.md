Does MongoDB support primary-key, foreign-key relationship

No. By Default, MongoDB doesn't support primary key-foreign key relationship. Relationships in the traditional sense don’t really exist in MongoDB.

We can work with related data by two approaches:

- Reference Based Relationships (Normalization) 
It feels similar to how things might be done in a relational database, but relationship is *not* enforced – unlike a relational database that enforces data integrity across relationships.

To reference a document in Mongoose, you can use

```js 
const gameSchema = new mongoose.Schema({
    title: String,
    publisher: {
        type: mongoose.Schema.Types.ObjectId,
        ref: 'Publisher'
    }
});

// to make a join use populate
async function listGames() {
    const games = await Game
        .find()
        .populate('publisher')
        .select('title publisher');
    console.log(games);
}

listGames();
```

- Embedded Documents Relationships (Denormalization).

To embed a sub document with mongoose

```js 
const gameSchema = new mongoose.Schema({
    title: String,
    publisher: {
        type: new mongoose.Schema({
            companyName: String,
        })
    }
})
```


