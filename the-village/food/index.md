---
layout: default
---

# The Village - Food


### Concepts and Idea for Food

* Seperate individual food inventories (on person, in storage, etc)
* Seperate collection to store food item definitions

* Items in the 'FoodItems' collection can be simple component items like apples, floor, sugar, etc or more complex items made up of sub-items, like "Apple Pie".

* Items can be multi-portions
	* Stats will be per individual portion
	* Ingredient quantities will be for the whole item

### Example

* One apple pie would be added to an inventory, possibly as "apple pie slice".  
* Each slice would inherit the stats for the whole (stats are listed for portions).  
* The ingredients listed would be to make one apple pie, (6 slices).
* Eating one slice of pie would give a +10 towards hunger.


### Hunger


### Thirst

### Stamina

### HungerSaturation

* Used to calculate when hunger should start to deplete again

* NOTE:  Not sure how I'm going to do this exactly, but I want some way to indicate that "bad" food may fill you up but not keep you from being hungry for too long.


### Happiness 

<pre>
<code>
FoodItems:
		name:        String,
		nameFormal:  String,
		portions:    Number
		stats:  {
					hunger: 			Number,
					thirst:				Number,
					stamina: 			Number,
					hungerSaturation: 	Number,
					happiness: 			Number	
				},
		cooked:      Boolean,
		complex:     Boolean,
		ingredients: [
				{
					foodItem: { type: Schema.Types.ObjectId, ref: 'fooditems' },
					quantity: Number
				}
			]
</code>
</pre>

<pre>
<code>
	name: "Apple",
	nameFormal: "apple",
	portions: 1,
	stats: {
				hunger: 1,
				thirst: 1,
				stamina: 1,
				hungerSaturation: 1,
				happiness: 1
			},
	cooked: false,
	complex: false,
	ingredients: []
	
	-------------------------------------------------------

	name: "Apple Pie",
	nameFormal: "apple_pie",
	portions: 6,
	stats: {
				hunger: 10,
				thirt: 2,
				stamina: 10,
				hungerSaturation: 10,
				happiness: 10
			},
	cooked: true,
	complex: true,
	ingredients: [
		{ foodItem: ObjectId(''), quantity: 10 }, // Apples
		{ foodItem: ObjectId(''), quantity: 3},  // Flour
		{ foodItem: Object(''), quantity: 2}, // Eggs
		{ foodItem: Object(''), quantity: 1}, // Sugar
	]

	-------------------------------------------------------

	name: "Apple Juice",
	nameFormal: "apple_juice",
	portions: 1,
	stats: {
				hunger: 1,
				thirst: 5,
				stamina: 1,
				hungerSaturation: 1,
				happiness: 2
			},
	cooked: false,
	complex: false,
	ingredients: [
		{ foodItem: ObjectId(''), quantity: 1 }, // Apples
		{ foodItem: ObjectId(''), quantity: 1 },  // Sugar
		{ foodItem: ObjectId(''), quantity: 1 },  // Water
	]
</code>
</pre>