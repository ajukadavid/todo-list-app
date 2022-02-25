<template>
<div>
<li
v-for="todo in todos"
:key="todo"
>
{{ todo.name }}
</li>
</div>
</template>

<script>
export default {
  props: ['todos']
}
</script>

<style scoped>

</style>
