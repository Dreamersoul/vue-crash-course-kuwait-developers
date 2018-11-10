<template>
  <div class="hello">
    <h1>My List</h1>
    <ol>
      <todo-item
        v-for="item in todos"
        v-bind:todo="item"
        v-bind:key="item.id">
      </todo-item>
    </ol>
  </div>
</template>

<script>
import TodoItem from './TodoItem.vue'

export default {
  name: 'HelloWorld',
  components: {
    TodoItem
  },
  data: function(){
    return {
      todos:[
        {id: 1, text: "todo No. 1"},
        {id: 2, text: "todo No. 2"},
        {id: 3, text: "todo No. 3"},
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
input {
      width: 30%;
      padding: 12px 12px;
    margin: 8px 0;
    box-sizing: border-box;
}
ol {
  padding: 0px;
  list-style-position: inside;
}
li {
  margin: 0 10px;
}
</style>
