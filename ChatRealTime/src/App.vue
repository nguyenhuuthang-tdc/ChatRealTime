<template>
  <div id="app">
    <comp-header 
      v-bind:titleHeader="titleHeader"
      v-on:changeTitleEvent="changeTitleEvent"
    />
    <list-user v-bind:listUser="Users" />
    <comp-footer v-bind:titleHeader="titleHeader" />
  </div>
</template>

<script>
import CompHeader from './components/CompHeader.vue'
import ListUser from './components/ListUser.vue'
import CompFooter from './components/CompFooter.vue'
export default {
  name: 'app',
  data () {
    return {
      titleHeader: "Header of Page, VueJs Welcome",
      // titleFooter: "Footer of Page, VueJs Goodbye",
      //array of object user
      Users: [
        {id: 1,name: "Huu Thang", active: false},
        {id: 2,name: "Minh Tri", active: false},
        {id: 3,name: "Suong", active: true},
        {id: 4,name: "Tho", active: false},
        {id: 5,name: "Son", active: true},
      ]
    }
  },
  components: {
    CompHeader,
    ListUser,
    CompFooter,
  },
  methods: {
    changeTitleEvent() {
      this.titleHeader = "Thắng ngu vãi đái";
    }
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
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
