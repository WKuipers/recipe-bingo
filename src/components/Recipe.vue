<template >
  <div 
    class="RecipeCard"
  >
    <h2>{{title}}</h2>
    <p> {{description}} </p>
    Resources:
    <ul>
     <li v-for="link in links" v-bind:key="link">
       <a v-bind:href="link">{{link}}</a>
     </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'RecipeCard',
  props: {
    title: String,
    description: String,
    links: Array[String], 
  },
}
</script>

<style scoped>
.RecipeCard {
  border-style: solid;
}
</style>
