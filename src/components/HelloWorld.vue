<template>
  <div class="hello">
    <b-navbar toggleable type="light" variant="light">
        <b-navbar-toggle target="nav_text_collapse"></b-navbar-toggle>
        <b-navbar-brand>BootstrapVue</b-navbar-brand>
        <b-collapse is-nav id="nav_text_collapse">
            <b-navbar-nav>
                <b-nav-text>Navbar text</b-nav-text>
            </b-navbar-nav>
        </b-collapse>
    </b-navbar>
    <div class="container">
      <b-alert show variant="primary">Primary Alert</b-alert>
      <b-btn v-b-modal.modal1>Launch demo modal</b-btn>
      <div class="my-3">
        <b-btn v-b-popover.hover="'I am popover content!'" title="Popover Title">
          Hover Me
        </b-btn>
      </div>
      <b-table striped hover :items="items"></b-table>
    </div>
    <!-- Modal Component -->
    <b-modal id="modal1" title="Bootstrap-Vue">
      <p class="my-4">Hello from modal!</p>
    </b-modal>
  </div>
</template>

<script>
  import Vue from 'vue'
  import BootstrapVue from 'bootstrap-vue'
  import 'bootstrap/dist/css/bootstrap.css'
  import 'bootstrap-vue/dist/bootstrap-vue.css'

  Vue.use(BootstrapVue);
const items = [
  { isActive: true, age: 40, first_name: 'Dickerson', last_name: 'Macdonald' },
  { isActive: false, age: 21, first_name: 'Larsen', last_name: 'Shaw' },
  { isActive: false, age: 89, first_name: 'Geneva', last_name: 'Wilson' },
  { isActive: true, age: 38, first_name: 'Jami', last_name: 'Carney' }
]
  export default {
    name: 'HelloWorld',
    components: {
      BootstrapVue
    },
    data: function () {
      return {
        items: items
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