---
layout: default
---

# The Village - Food


### Concepts and Idea for Food

* Seperate individual food inventories (on person, in storage, etc)
* Seperate collection to store food item definitions

* Items in the 'FoodItems' collection can be simple component items like apples, floor, sugar, etc



<pre>
<code>
FoodItems:
		name:        String,
		nameFormal:  String,
		portions:    Number
		stats:  {
					hunger: 			Number,
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
</code>
</pre>