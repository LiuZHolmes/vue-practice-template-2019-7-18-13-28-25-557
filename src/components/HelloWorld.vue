<template>
  <div class="hello">
    <counter-group v-on:change-sum="changeSum" v-on:countSum="countSum" :initialCount="2"></counter-group>
    <span>{{sum}}</span>
  </div>
</template>

<script>
import CounterGroup from './CounterGroup.vue'
export default {
  name: 'HelloWorld',
  data() {
    return {
      count: 1,
      sum : 0
    }
  },
  methods: {
    countSum(num) {
      this.sum += num;
    },
    changeSum(num) {
      this.sum = num;
    }
  },
  components: {
    CounterGroup
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
