<template>
  <div class="bg-green-100 h-screen">
    <Nav/>
    <Form @addTodo="addTodo"/>

    <TodoItem :todos="todos" v-if="todos !== []"/>
  </div>

</template>

<script>
export default {

  data() {
    return {
      todos: [

      ]
    }
},
methods: {
    addTodo(value){
      this.todos.push(value)
    }
}
}
</script>
