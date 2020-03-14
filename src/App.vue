<template>
  <Todo v-bind:todos="todos" />
</template>



<script>
import Todo from './components/Todo.vue'

export default {
  name: "App",
  components: {
    Todo
  },
  data() {
    return {
      todos: [{
        id:1,
        title:"Go to the gym",
        completed:false,
      },{
        id:2,
        title:"Do some work",
        completed:true,
      },{
        id:3,
        title:"Say hi to sivan",
        completed:true,
      }]
    };
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

//sk.eyJ1IjoiYWhtZWRidXJoYW4iLCJhIjoiY2s3cmdyZ3F4MGNiZDNubnZyczE3bTYyayJ9.znB_bf2q4wWod-EJigbkwg
