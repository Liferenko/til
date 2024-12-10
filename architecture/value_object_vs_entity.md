## Value Object vs Entity

Entity might have few attributes and always has a unique ID.
Value Object is a small object that represents a simple entity whose equality is not based on ID.


Two value objects with same attributes are equal. They are the same if they have the same attributes.
Two entities with same attributes are not equal. They are the same if they have the same ID.
