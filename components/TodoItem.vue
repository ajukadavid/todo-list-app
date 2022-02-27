<template>
<div>
  <ul>
    <li
      v-for="(todo, index) in todos"
      :key="todo"
    >
    <input type="checkbox" id="todo" name="todo" :value="todo">
     <span class="text-3xl">{{ todo }} </span>
      <button @click="deleteTodo(index)">Delete item</button>
    </li>

  </ul>

</div>
</template>

<script>
export default {
  props: ['todos'],
  methods: {
    deleteTodo(index){
      this.todos.splice(index, 1)
    }

  }

}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Shizuru&display=swap');
li {
  list-style-type: none;
  display: flex;
  justify-content: space-between;
}
div {
  background-color: #6ee7b7;
  margin: auto;
  width: 60%;
  border: 5px solid #ecfdf5;
  padding: 10px;
}
span {
  font-size: 28px;
  font-family: 'Shizuru', cursive;

}
button {
  border: 1px solid aquamarine;
  background-color: #065f46;
  padding: 10px;
  border-radius: 1rem;
  color: white;
  margin: 8px;
  font-size: 18px;
  font-family: 'Shizuru', cursive;
}
</style>
