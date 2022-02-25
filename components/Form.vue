<template>
      <div class="shadow-inner border-solid border-2 border-green-100 my-8 grid place-items-center">
        <label for="item" class="m-8 p-4 tracking-widest text-3xl">New Todo Item</label>
        <input id="item" class="shadow-md p-4" type="text" placeholder="Your todo item" v-model="todo"/>
        <button @click="addTodo" class="p-4 rounded-md border-double border-2 hover:border-green-500 m-8">Add Item</button>
      </div>
</template>

<script>
export default {
  data(){
    return {
      todo: ''
    }
  },
  methods: {
    addTodo(){
      this.$emit('addTodo', this.todo)
    }
  }
}
</script>

<style scoped>

</style>
