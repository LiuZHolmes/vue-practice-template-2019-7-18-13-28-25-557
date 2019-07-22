<template>
  <div class="hello">
     <span><input v-on:input="countSum" v-model.number="count"></span>
     <Counter ref="counters" v-for="n in count" :key="n"></Counter>
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
    countSum() {
        let sum = 0;
        let counters = this.$refs.counters;
        let length = Math.min(this.count,counters.length)
        for (let i = 0; i < length; i++) {
            sum += counters[i].num;
        }
      this.$store.commit('setSum',sum);
    }
  },
  components: {
    Counter
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
