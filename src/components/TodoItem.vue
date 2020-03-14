<template>
  <div v-bind:class="{'isCompleted':todo.completed}" >
    <p>{{todo.title}}</p>
  </div>
</template>

<script>

export default {
  name:"TodoItem",
  props:["todo"]
}
</script>

<style>
  .isCompleted{
    text-decoration: line-through;
  }
</style>