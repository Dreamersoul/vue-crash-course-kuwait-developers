<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h1>{{ capitalizedMsg }}</h1>
    <input type="text" v-model="msg" />
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data: function(){
    return {
      msg: ""
    }
  },
  computed: {
    capitalizedMsg(){
      return this.msg.toUpperCase();
    }
  }
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
