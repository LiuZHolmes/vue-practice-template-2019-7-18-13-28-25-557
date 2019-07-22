<template>
  <div class="hello">
    <counter-group :initialCount="2"></counter-group>
    <span>{{sum}}</span>
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
  computed: {
    sum() {
      return this.$store.state.sum;
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
