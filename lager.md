Light Lager
===========

Adapted from [John
Palmer](http://www.howtobrew.com/section4/chapter19-4.html)


Water
------
+/- 2 gallons of distilled ( mix with regular tap )


Fermentables
------------
1. [6 lbs Pilsen Malt
   Syrup](http://www.northernbrewer.com/shop/northern-brewer-pilsen-malt-syrup.html)
2. [2 lbs Rahr
   2-Row](http://www.northernbrewer.com/shop/brewing/brewing-ingredients/grain-malts/rahr-2-row.html)

Hops
---------
[1 oz Perle](http://www.northernbrewer.com/shop/perle-pellets-1-oz.html)
[3 oz Czech
Saaz](http://www.northernbrewer.com/shop/saaz-pellets-1-oz.html)


Yeast
-----
[Wyeast 2001 Pilsner
Urquell](http://www.northernbrewer.com/shop/brewing/brewing-ingredients/beer-yeast/wyeast-pilsner-urquell.html)

Extras
------
[Priming sugar](http://www.northernbrewer.com/shop/priming-sugar.html)


##Directions

Preform a small mash with the 2lbs or Rahr 2-Row.

Use 2qt of water.

* Mash in @ 125F for 20 minutes
* Monster mash @ 140F for 30 minutes
* Mash out @ 158F for 30 minutes

Lauter out the mash with 1 recirculation.

Prepare boil kettle with ~2qts of mashed wort with additional water to
bring the total to 3 gallons.

Bring solution to a boil.
```javascript
kettle.addEventListener('boil', function(){
  remove from heat;
  mix 6 lbs of Pilsen Malt into solution;
  kettle.fireEvent('resumeBoil');
}

kettle.addEventListener('resumeBoil', function(){
  resume boil for 69 minutes;
  kettle.fireEvent('hopEvent1');
  setTimeout(function(){ kettle.fireEvent('hopEvent2');}, 30 min);
  setTimeout(function(){ kettle.fireEvent('hopEvent3');}, 45 min);
}

kettle.addEventListener('hopEvent1', function(){
  add 1 oz perle
});
kettle.addEventListener('hopEvent2', function(){
  add 2 oz Saaz
});
kettle.addEventListener('hopEvent3', function(){
  add 1 oz Saaz
});
```

Cool down under 80F and place in fermenter.

With a lager, the fermentation temp needs to be between 45F - 54F 
**DO NOT ADD YEAST UNTIL WORT IS IN TEMP RANGE**

Typically fermentation schedule 2 weeks => primary, 2 weeks =>
secondary, 2 weeks => bottle conditioning.
