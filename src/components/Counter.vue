<template>
  <div class="hello">
     <span><input type="button" v-on:click="sub" value="-"></span>
     <span> {{num}} </span>
     <span><input type="button" v-on:click="add" value="+"></span>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: Number
  },
  data() {
    return {
      num: 0
    }
  },
  methods: {
    sub() {
      this.num--;
    },
    add() {
      this.num++;
    }
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
