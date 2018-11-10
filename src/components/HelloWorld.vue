<template>
  <div class="hello">
    <div v-if="seen">Now you see me</div>
    <div v-else>Now you can’t</div>
    <button v-on:click="toggleSeen">Toggle seen</button>

    <ol>
      <li v-for="todo in todos">
        {{ todo.text }}
      </li>
    </ol>
    <input v-model="newTodo" type="text" @keyup.enter="addTodo" placeholder="enter a todo and press enter to append it">
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data: function(){
    return {
      newTodo: "",
      seen: true,
      todos:[
        {text: "todo No. 1"},
        {text: "todo No. 2"},
        {text: "todo No. 3"},
      ]
    }
  },
  methods: {
    toggleSeen(){
      this.seen = !this.seen;
    },
    addTodo(){
      if(this.newTodo){
        this.todos.push({text: this.newTodo});
        this.newTodo = "";
      }
    }
  }
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
