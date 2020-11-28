<template >
  <ul>
    <Recipe 
     v-for="recipe in recipes"
     :key="recipe"
     v-bind:title="recipe.title"
     v-bind:description="recipe.description"
     v-bind:links="recipe.links"
    />
  </ul>
</template>

<script>
import Recipe from './Recipe.vue'

export default {
  name: 'RecipeList',
  components: {Recipe},
  props: {
    recipes: Object
  },
}
</script>

<style scoped>
</style>
