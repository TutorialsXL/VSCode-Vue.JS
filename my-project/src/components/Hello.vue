<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2 v-bind:title="tooltip" v-bind:class="css">{{ employee }}</h2>
    <input type="button" @click="changeCss()" value="Change Color"/>
    </div>
</template>

<script>
  export default {
    name: 'hello',
    data() {
      return {
        msg: 'Welcome to Your Vue.js App',
        employee: 'David James',
        tooltip:'Hey I\'m a tooltip',
        css:'red'
      }
    },
    methods: {
      changeCss:function(){
        this.css = "blue";
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.red{
  color:red;
}
.blue{
  color:blue;
}
</style>