<template>
  <div id="app">
    <h1>Cook's Guild December Bingo</h1>
    <p>
      Click on a square to view the recipe, and click again to mark it as done.
      The top row is vegan, but feel free to make versions of any dish catered to your dietary preferences.
    </p>
    <h2>Cook's bingo:</h2>
    <BingoCard v-bind:recipes="recipes"/>
    <BingoConnector 
    v-bind:recipes="recipes"/>
  </div>
</template>

<script>
import BingoConnector from './components/BingoConnector.vue'
import BingoCard from './components/BingoCard.vue'

export default {
  name: 'App',
  components: {
    BingoConnector,
    BingoCard
  },
  data: function() {
    let recipes = {
      'stock': {
        title: 'Make your own stock',
        description: 'A good stock is the basis of many dishes. A vegetable stock is the easiest to start with, but chicken stock is easy as well.',
        links: ['https://www.seriouseats.com/recipes/2015/11/quick-and-easy-vegetable-stock-recipe.html', 'https://www.youtube.com/watch?v=Vu7f24XWj1k']
      },
      'bread': {
        title: 'Bake bread from scratch',
        description: 'Good bread requires patience, good ingredients and some effort.',
        links: ['https://www.seriouseats.com/recipes/2014/08/simple-crusty-white-bread-recipe.html']
      },
      'spaghetti': {
        title: 'Spaghetti Aglio e Olio',
        description: 'A typical dish from Naples. For best results use a quality Italian pasta brand and fresh garlic',
        links: ['https://www.youtube.com/watch?v=bjmYkPkjnVo']
      },
      'fries': {
        title: 'Fries',
        description: 'A classic dish where technique and the recipe makes all the difference.',
        links: ['https://www.seriouseats.com/recipes/2009/06/perfect-french-fries-recipe.html', 'https://www.spendwithpennies.com/crispy-oven-fries/']
      },
      'hummus': {
        title: 'Hummus',
        description: 'Hummus is a Middle East staple that can be used as a spread, dip or as a dish.',
        links: ['https://www.seriouseats.com/recipes/2012/11/basic-hummus-from-jerusalem-ottolenghi.html']
      },
      'pannacotta': {
        title: 'Panna Cotta',
        description: 'A light and elegant Italian dessert with endless variations',
        links: ['https://www.bbc.co.uk/food/recipes/vanillapannacotta_87907']
      },
      'omelette': {
        title: 'French omelet',
        description: 'A French breakfast staple, which can be filled to create a hearty meal',
        links: ['https://www.bonappetit.com/test-kitchen/how-to/article/perfect-french-omelet-hint-will-butter']
      },
      'muffins': {
        title: 'Muffins',
        description: 'An American baked treat, sweet and fluffy',
        links: ['https://www.seriouseats.com/recipes/2016/07/classic-blueberry-muffin-recipe.html']
      },
      'stoofpeertjes': {
        title: 'Stoofpeertjes (Poached pears)',
        description: 'A Dutch winter specialty, the best are sweet, tangy with still a bit of bite',
        links: ['https://www.liveeatlearn.com/poached-pears/']
      },
      'flammkuchen': {
        title: 'Flammkuchen',
        description: "A German savoury pizza, use store bought pizza dough if you don't want to make your own",
        links: ['https://www.seriouseats.com/2015/02/how-to-make-tarte-flambee-alsatian-pizza-bacon-quick-bar-style-classic.html']
      },
      'applecrumble': {
        title: 'Apple crumble',
        description: 'An easy, classic and fruity dessert. Apples are the standard, but most hard fruits will work',
        links: ['https://www.jamieoliver.com/recipes/fruit-recipes/classic-apple-crumble/']
      },
      'onigiri': {
        title: 'Onigiri',
        description: 'A Japanese rice snack with endless variations. Remember to use sushi rice!',
        links: ['https://www.seriouseats.com/2011/01/how-to-make-onigiri-japanese-sushi-rice-balls.html']
      },
      'sour': {
        title: 'Any "Sours" cocktail',
        description: 'This cocktail is over a hundred years old but still popular. Feel free to make it non-alcoholic',
        links: ['https://en.wikipedia.org/wiki/Sour_(cocktail)', 'https://www.youtube.com/watch?v=sbloHsAFqXY'],
      },
      'coleslaw': {
        title: 'Coleslaw',
        description: 'A famous American BBQ side-dish, a great addition to bring freshness to any heavy meal',
        links: ['https://www.seriouseats.com/recipes/2013/07/creamy-cole-slaw.html', 'https://www.inspiredtaste.net/26522/coleslaw-recipe/']
      },
      'quesadilla': {
        title: 'Quesadilla',
        description: 'The essential Mexican snack: Crispy, cheesy and filling. You can experiment with different fillings and sauces',
        links: ['https://www.seriouseats.com/recipes/2017/02/spicy-chicken-quesadilla-recipe.html', 'https://www.simplyrecipes.com/recipes/quesadilla/']
      },
      'garlicsoup': {
        title: 'Sopa de Ajo (Spanish garlic soup)',
        description: 'A hearty Spanish soup with bread, ham and of course garlic',
        links: ['https://www.youtube.com/watch?v=fixHiTWKRWA']
      }

    }
    return { recipes: recipes }
  }
}
</script>
