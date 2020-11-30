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
import recipes from './recipes.js'

export default {
  name: 'App',
  components: {
    BingoConnector,
    BingoCard
  },
  data: function() {
    return { recipes: recipes }
  }
}
</script>
