<template>
  <RecipeList v-bind:recipes="active_recipes"/>
</template>
<script>
import RecipeList from './RecipeList.vue'

export default {
  name: 'BingoConnector',
  components: {RecipeList},
  props: {
    recipes: Object
  },
  data: function() {
    return { active_recipes: {} }
  },
  mounted() {
    this.$root.$on('select', (id) => {
      this.$set(this.active_recipes, id, this.recipes[id])
    })
    this.$root.$on('unselect', (id) => {
      this.$delete(this.active_recipes, id)
    })
  }
}
</script>
