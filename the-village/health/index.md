---
layout: default
---

# Health

** This is a planned feature **

So one big component that I have planned with The Village is a health system for each villager/person. This will cover nutrition, sickness, physcial fitness, etc. For the nutrition, what each villager eats and drinks will have an impact on their overall health. So for instance if there is nothing to eat by twigs and berries, the over all health of the population might not be so good. However if they have been able to hunt and grow food then they will probably be doing better.

Since I haven't decided on the exact details of the end of this as far as timelines of the game (does it take place hunderds of years ago in a rural setting, modern times, the future) I'm trying to make the "engine" as generic and flexible as possible. In other words, didn't types of "food" can be given but that item will have certain generic values that the person's code will understand. That way I can program the food portion of the code to be berries, simple breads, or even pizza

For the illness portion I want to have include both short term illnesses (a cold) to more long lasting/chronic dieseases. These will eventually impact their productiveness, growth, and ability to survive.

<pre>
<code>
    health : {
    	hunger :		Number,
    	hungerSaturation:	Number,
    	thirst : 		Number,
    	stamina:		Number,
    	bmi:			Number,
    	inShape:		Number,
    	illness:		Number,
    	bodyTemp:		Number,
    	sleepiness:		Number
    }
</code>
</pre>


* [Hunger](hunger.html)