---
layout: default
---

# Height

***
<br />

Each person is grows from birth until age 20. A height bias determines how much below or above average the person will grow.  

Average age to height/weight values are used in combination with the bias to determine the height at each age.

The bias can be a value of 1-10, with 5 being average, 1 being extremely below average, and 10 being extremely above average.


* height(dad, mom, gender, callback) 
* getHeightGrowth(heightBias, averageDelta)
* determineHeightBias(dadBias, momBias)


<pre>
<code>
growth = averageDelta + (averageDelta * .15);
</code>
</pre>

<pre>
<code>
function determineHeightBias(dadBias, momBias)
{
    var height = {};
    var heightBias;

    var parentsBias = (dadBias + momBias) / 2;    
    var logBias = getBaseLog((Math.random() * 50) + 2, 9);
    var negRandNum = Math.round(Math.random());
    
    if(negRandNum === 1) { logBias *= -1}    	

    heightBias = parentsBias + logBias;

	if(heightBias < 1 ) heightBias = 1;
	if(heightBias > 10 ) heightBias = 10; 

	heightBias = Math.floor(heightBias);

	return heightBias;
}
</code>
</pre>

<pre>
<code>
{ "men": 
	[
		{ "year": 0,  "height": 20, "weight": 7 },
		{ "year": 1,  "height": 30, "weight": 21 },
		{ "year": 2,  "height": 34, "weight": 27 },
		{ "year": 3,  "height": 37, "weight": 31 },
		{ "year": 4,  "height": 40, "weight": 40 },
		{ "year": 5,  "height": 43, "weight": 40 },
		{ "year": 6,  "height": 45, "weight": 45 },
		{ "year": 7,  "height": 48, "weight": 50 },
		{ "year": 8,  "height": 50, "weight": 56 },
		{ "year": 9,  "height": 52, "weight": 63 },
		{ "year": 10,  "height": 54, "weight": 70 },				
		{ "year": 11,  "height": 56, "weight": 79 },
		{ "year": 12,  "height": 58, "weight": 88 },
		{ "year": 13,  "height": 62, "weight": 100 },
		{ "year": 14,  "height": 64, "weight": 112 },
		{ "year": 15,  "height": 67, "weight": 123 },
		{ "year": 16,  "height": 68, "weight": 134 },
		{ "year": 17,  "height": 69, "weight": 142 },
		{ "year": 18,  "height": 69, "weight": 147 },
		{ "year": 19,  "height": 70, "weight": 152 },			
		{ "year": 20,  "height": 70, "weight": 155 }	
	],

"women":

	[
		{ "year": 0,  "height": 20, "weight": 7 },
		{ "year": 1,  "height": 30, "weight": 20 },
		{ "year": 2,  "height": 34, "weight": 27 },
		{ "year": 3,  "height": 37, "weight": 32 },
		{ "year": 4,  "height": 40, "weight": 34 },
		{ "year": 5,  "height": 43, "weight": 40 },
		{ "year": 6,  "height": 46, "weight": 44 },
		{ "year": 7,  "height": 48, "weight": 50 },
		{ "year": 8,  "height": 51, "weight": 57 },
		{ "year": 9,  "height": 53, "weight": 62 },
		{ "year": 10,  "height": 54, "weight": 71 },				
		{ "year": 11,  "height": 58, "weight": 82 },
		{ "year": 12,  "height": 59, "weight": 91 },
		{ "year": 13,  "height": 62, "weight": 101 },
		{ "year": 14,  "height": 62, "weight": 105 },
		{ "year": 15,  "height": 63, "weight": 115 },
		{ "year": 16,  "height": 64, "weight": 118 },
		{ "year": 17,  "height": 64, "weight": 120 },
		{ "year": 18,  "height": 64, "weight": 125 },
		{ "year": 19,  "height": 64, "weight": 126 },			
		{ "year": 20,  "height": 64, "weight": 128 }
	]
}
</code>
</pre>