# JPA elementcollection tillåts inte i embeddeble

JSR-317 2.6 Collections of Embeddable Classes and Basic Types An embeddable class (including an embeddable class within another embeddable class) that is contained within an element collection must not contain an element collection, nor may it contain a relationship to an entity other than a many-to-one or one-to-one relationship
