# Metadata-Management

We value software craftsmanship a lot, and we believe that the quality of the developer can be judged by the quality of the code and the discussion about the choices made. Please do this exercise yourself (as a candidate) without the help of colleagues.

What we expect from you:

- A public git repository stored in GitHub, Bitbucket, Gitlab, etc.
- A fully working application developed with Node.js. Feel free to use the libraries you want
- We expect a [README.md](http://readme.md/) that explains how to compile and run this code.
- We expect you to spend at least a few days on this. But, of course, this is up to you.

Requirements:

- The application must be working on its own, with practically no intervention (this means not having to use our own tools to do the code work)

Highly Valuable:

- Use a containerization system that will allow the infrastructure to be raised.
- At least a unit testing layer that covers your implementation.
- DDD, CQRS and Hexagonal Architecture are highly valuables

### **Exercise**

A card store is tired of calling the supplier to check what cards they have and which ones are not available. To fix this,  they hired you to make your own card management app. Of course, you can not make up any card you think and to get the actual cards, they provide you an API with all the cards.

The application consists of 5 processes:

1. Parse the metadata for the cards: This part will be done by reaching this API [REST API Documentation](https://scryfall.com/docs/api). The store owner is highly interested in these 3 collections:
    - Ikoria: Lair of Behemoths (IKO)
    - Guilds of Ravnica (GRN)
    - Innistrad (ISD)
2. The owner doesn’t want every metadata that API has. He’s only interested in the following data:
    1. Name
    2. Language
    3. Release date
    4. Images (as URLs)
    5. Collection of that card (which set this card is part of)
    6. Game legalities
3. Also, we are sure that some cards are reprinted, but we aren’t interested in them. So if any two cards are the same cards, we only want to store the newer one
4. We need to store all this data within a database. You’re free to set up the one you like the most.
5. We need a way to interact with this database to get:
    1. All the cards of a collection
    2. A card by knowing its id
    3. A query to search a specific card by its name
    4. All cards that are legal in X game mode

This interaction layer could be done through a FrontEnd or a CLI tool. If the second is the case, make sure that the instructions to use it are set in the Readme file
