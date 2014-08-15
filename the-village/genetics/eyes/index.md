---
layout: default
---

# Eyes

***


Eyes can be one of three colors:

* brown
* green
* blue

Eye information is stored in the database for each person under: genome > genes > eyes.

The following information is stored:

* color ("brown", "green", or "blue")
* bey2
	* one ("Allele" info taken from the father)
	* two ("Allele" info taken from the mother)
* gey
	* one
	* two

<pre>
<code>
	eyes: {
		color: String,
		bey2 : {
			one: String, two: String
		},
		gey :  {
			one: String, two: String
		}
	},
</code>
</pre>

When each person is "born" a random "allele" ("one" or "two") is picked for each parent, to simulate (in a very simple way) how it would work with real genetics.  After the "bey2" and "gey" genes are chosen, a seperate function figures out what the eye color should be based on dominance.

Possible pairs:

* brown-brown
* brown-blue
* blue-blue

* green-green
* green-blue
* blue-blue

<pre>
<code>
	if(bey2.one === "brown" || bey2.two === "brown") {
		return "brown";
	} else if (gey.one === "green" || gey.two === "green") {
		return "green";
	} else {
		return "blue";
	}
</code>
</pre>

![Genetics](http://blutekus.net/uploads/screen_village_20140805a.png)