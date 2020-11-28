<template>
<div class="bingo">
    <BingoSpace class="space"
         v-for="(recipe, id) in recipes"
         :key="id"
         v-bind:text="recipe.title"
         v-bind:id="id"
    />
</div>
</template>
<script>
import BingoSpace from './BingoSpace.vue'

export default {
  name: 'BingoGrid',
  components: {BingoSpace},
  props: {
    recipes: Object
  },
}
</script>

<style scoped>
.bingo {
  display: grid;
  grid-template-columns: repeat(4, auto);
  max-width: 800px;
  grid-gap: 2px;
}

.space {
  display: flex;
  padding: 5px;
  text-align: center;
  justify-content: center;
  align-items: center;
  outline: 2px solid black;
}
</style>
