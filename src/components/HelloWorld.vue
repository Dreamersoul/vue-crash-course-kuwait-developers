<template>
  <div class="hello">
    <span v-if="seen">Now you see me</span>
    <span v-else>Now you can’t</span>

    <ol>
      <li v-for="todo in todos">
        {{ todo.text }}
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data: function(){
    return {
      seen: true,
      todos:[
        {text: "todo No. 1"},
        {text: "todo No. 2"},
        {text: "todo No. 3"},
      ]
    }
  },
}
</script>

<style scoped>
.hello {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  
}
ol {
  padding: 0px;
  list-style-position: inside;
}
li {
  margin: 0 10px;
}
</style>
