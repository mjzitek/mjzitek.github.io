---
layout: default
---

# Hair

***
<br />

### Initial Population Creation

For the initial population creation , hair colors are randomly chosen by choosing a "one" and "two" value and then using the normal function of randomly selecting one or two.

![Genetics](http://blutekus.net/uploads/village-haircolors.png)

<pre>
<code>
	hair.one = dadHairAllele;
	hair.two = momHairAllele;
	hair.color = getRandomAllele(hair);	
</code>
</pre>

For babies, a similar process is used to the other attributes of selecting a random "allele" from each parent.

<pre>
<code>
	var dadHairAllele = getRandomAllele(dad.genome.genes.hair);
	var momHairAllele = getRandomAllele(mom.genome.genes.hair);
</code>
</pre>

<pre>
<code>
	hair: {
			color:  { R: Number, G: Number, B: Number },
			one:  { R: Number, G: Number, B: Number },
			two:  { R: Number, G: Number, B: Number },
	      },
</code>
</pre>


<pre>
<code>
function hairColors(num) {

	var colors = [
		{ R: 9,   G: 8,   B:6   },	
		{ R: 59,  G: 48,  B:36  },	
		{ R: 78,  G: 67,  B:63  },	
		{ R: 85,  G: 72,  B:56  },
		{ R: 106, G: 78,  B:66  },
		{ R: 167, G: 133, B:106 },
		{ R: 149, G: 83,  B:52	},
		{ R: 109, G: 41,  B:6	},
		{ R: 229, G: 110, B:51  },
		{ R: 242, G: 245, B:193 },
	];


	return colors[num];
}
</code>
</pre>






![Genetics](http://blutekus.net/uploads/screen_village_20140805a.png)
