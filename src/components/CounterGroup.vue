<template>
  <div class="hello">
     <span><input v-model.number="count"></span>
     <Counter v-for="n in count" :key="n"></Counter>
  </div>
</template>

<script>
import Counter from './Counter.vue'
export default {
  name: 'CounterGroup',
  props: {
      initialCount: Number
  },
  data() {
    return {
       count: this.initialCount
    }
  },
  methods: {
    
  },
  components: {
    Counter
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
