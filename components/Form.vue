<template>
      <div class="wrapper shadow-inner border-solid border-2 border-green-100 my-8 grid place-items-center">
        <label for="item" class="m-8 p-4 tracking-widest text-3xl">New Todo Item</label>
        <input id="item" class="text-field font-extrabold shadow-md p-4" type="text" placeholder="Your todo item" v-model="todo"/>
       <p v-if="isError" class="font-bold text-red-500">Please Input a todo item</p>
        <button @click="addTodo" class="p-2 rounded-3xl border-green-200 border-4 hover:rounded-md m-8">Add Item</button>
      </div>
</template>

<script>
export default {
  emits: ['addTodo'],
  data(){
    return {
      todo: '',
      isError: false
    }
  },
  methods: {
    addTodo(){
      if(this.todo !== ''){
        this.$emit('addTodo', this.todo)
        this.todo = ''
        this.isError = false
      } else {
        this.isError = true
      }
    }
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Shizuru&display=swap');

.wrapper {
  font-family: 'Shizuru', cursive;
}

.text-field {
  width: 400px;
}
</style>
