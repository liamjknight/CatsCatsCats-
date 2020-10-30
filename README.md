# CATS CATS CATS!

## project from Tech Elevator, completed by Liam Knight


* `GET /api/cards`: Provides a list of all Cat Cards in the user's collection.
* `GET /api/cards/{id}`: Provides a Cat Card with the given ID.
* `GET /api/cards/random`: Provides a new, randomly created Cat Card containing information from the cat fact and picture services.
* `POST /api/cards`: Saves a card to the user's collection.
* `PUT /api/cards`: Updates a card in the user's collection.
* `DELETE /api/cards`: Removes a card from the user's collection.

### Cat Card JSON object structure

Here's the JSON object structure for a Cat Card:

```
{
    "id" : an integer that represents this particular card's unique identifier,
    "imgUrl" : "A string containing the full URL to the cat image",
    "fact" : "A string containing a cat fact",
    "caption" : "A string containing the caption for this particular card"
}
```

### Cat Card collection example

Here's an example collection of Cat Cards:

```
[
    {
        "id" : 17,
        "imgUrl" : "https://purr.objects-us-east-1.dream.io/i/8M3AW.jpg",
        "fact" : "Cats sleep 70% of their lives.",
        "caption" : "Aww, this reminds me of Lefty! He slept CONSTANTLY."
    },

    {
        "id" : 38,
        "imgUrl" : "https://purr.objects-us-east-1.dream.io/i/image.jpeg",
        "fact" : "People who own cats have on average 2.1 pets per household, whereas dog owners have about 1.6.",
        "caption" : "Bartender, I'll take a Salty *Cat*"
    }
]
```

### Cat APIs

There are two web APIs tha provide this app resources.

`https://random-cat-image.herokuapp.com/` to retrieve a random cat picture.

`https://cat-fact.herokuapp.com/facts/random` to retrieve random cat facts.

Huge thanks, their GitHub is below.

`https://alexwohlbruck.github.io/cat-facts/docs/endpoints/facts.html`.

You should implement the `RestCatFactService` to call this endpoint and return the data as a `CatFact` object.

### Getting started

1. To install your database, run the command `database/create_db.sh`.

    **Note**: You'll see a message that says that the "catcards" table doesn't exist the first time you run the `create` script. You can ignore the message.

2. Launch this project by running it as a Spring Boot application and navigate to `http://localhost:8080`.

