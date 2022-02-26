<template>
  <div class="bg-green-100">
    <Nav/>
    <Form @addTodo="addTodo"/>

    <TodoItem :todos="todos"/>
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
