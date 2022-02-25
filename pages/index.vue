<template>
  <div>
    <Nav/>
    <Form />

    <TodoItem :todos="todos"/>
  </div>

</template>

<script>
export default {

  data() {
    return {
      todos: [
        {
          name: 'Do 2h Merch',
        },
        {
          name: 'Learn Vuex',
        },
        {
          name: 'Learn Typescript',
        }
      ]
    }
}
}
</script>
