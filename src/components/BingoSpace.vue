<template>
  <div v-bind:class="classObject" @click="select()">
    <b>{{text}}</b>
  </div>
</template>

<script>
export default {
  name: 'BingoSpace',
  props: {
    id: String,
    text: String,
  },
  data: function() {
    return {
       state: 0
    };
  },
  computed: {
    classObject: function() {
      return {
        inactive: this.state == 0,
        inprogress: this.state == 1,
        done: this.state == 2,
      }
    }
  },
  methods: {
    select() {
       this.state = (this.state + 1) % 3
       if (this.state == 1) {
           this.$root.$emit('select', this.id)
       } else {
           this.$root.$emit('unselect', this.id)
       }
    }
  }
}
</script>

<style scoped>
.inactive {
}
.inprogress {
  background-color: yellow;
}
.done {
  background-color: green;
}
</style>
