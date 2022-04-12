# Gilded Rose Testing and Refactoring Kata

Welcome to the Guilded Rose kata!

The objective in this excercise, is to take the code as provided, and by adding tests and refactoring the code make it more maintainable, leading to the addtion of a new feature.

While no tests are provided with the code, you **are expected to write unit tests to support your changes** and modify the code in any other way you see fit.

## The Problem

Welcome to team Gilded Rose!

We are a small inn with a prime location in a prominent city ran by a friendly innkeeper named Allison. We also buy and sell only the finest goods. Unfortunately, our goods are constantly degrading in quality as they approach their sell by date.

We have a system in place that updates our inventory for us. It was developed by a no-nonsense type named Leeroy, who has moved on to new adventures.

*Your task is to add the new feature to our system so that we can begin selling a new category of items.*

## What the program currently does

- All items have a SellIn value which denotes the number of days we have to sell the item
- All items have a Quality value which denotes how valuable the item is
- At the end of each day our system lowers both values for every item - petty simple, right?

Well this is where it gets interesting:

- Once the sell by date has passed, Quality degrades twice as fast
- The Quality of an item is never negative
- "Aged Brie" actually increases in Quality the older it gets
- The Quality of an item is never more than 50
- "Sulfuras", being a legendary item, never has to be sold or decreases in Quality

- "Backstage passes", like aged brie, increases in Quality as its SellIn value approaches;
  - Quality increases by 2 when there are 10 days or less and by 3 when there are 5 days or less but
  - Quality drops to 0 after the concert

Just for clarification, an item can never have its Quality increase above 50, however "Sulfuras" is a
legendary item and as such its Quality is 80 and it never alters.

## The new feature we need to implement

We have recently signed a supplier of conjured items.

This requires an update to our system:

- "Conjured" items degrade in Quality twice as fast as normal items

Feel free to make any changes to the UpdateQuality method and add any new code as long as everything
still works correctly. Your changes should be supported by appropriate tests.

However, do not alter the Item class or Items property as those belong to the
goblin in the corner and he doesn't believe in shared code ownership (you can make the UpdateQuality method and Items property static if you like, we'll cover for you).

## Hints

This is deliberately a production-like scenario.

- Treat it like a production system and test your code as you go
- Feel free to test existing behaviour
- Feel free to add new behaviour
- Added behaviour should be supported by tests

We use this kata to understand both your approach, and code style.
You're allowed to change anything in the sample submitted - we know this is bad code!
