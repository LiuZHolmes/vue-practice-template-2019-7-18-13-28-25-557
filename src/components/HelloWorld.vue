<template>
  <div class="hello">
    <counter-group v-bind:initialCount="12"></counter-group>
  </div>
</template>

<script>
import CounterGroup from './CounterGroup.vue'
export default {
  name: 'HelloWorld',
  data() {
    return {
      count: 1
    }
  },
  methods: {
    
  },
  components: {
    CounterGroup
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
