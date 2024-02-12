<script setup>
let id = 0

const newTodo = ref('')
const todos = ref([
  { id: id++, text: 'Learn HTML', done: true },
  { id: id++, text: 'Learn JavaScript', done: true },
  { id: id++, text: 'Learn Vue', done: false }
])

const addTodo = () => {
  todos.value.push({ id: id++, text: newTodo.value, done: false })
  newTodo.value = ''
}

const removeTodo = (todo) => {
  todos.value = todos.value.filter((t) => t !== todo)
}
</script>

<template>
  <div class="mx-auto my-10 bg-white p-6 w-3/4 rounded-md shadow-lg">
    <h1 class="text-3xl font-medium">Tasks list</h1>
    <div class="my-2 divide-y divide-slate-200">
      <div v-for="todo in todos" :key="todo.id"
        class="flex items-center justify-between py-3 px-2">
        <div class="inline-flex items-center">
          <input type="checkbox" v-model="todo.done"
            class="h-4 w-4 mr-2 rounded border-gray-300 text-indigo-600 focus:ring-indigo-300">
          <span :class="{ 'text-gray-400 line-through': todo.done }">{{ todo.text }}</span>
        </div>
        <button @click="removeTodo(todo)">
          <IconsTrash class="text-slate-600 text-xl" />
        </button>
      </div>
    </div>
    <form @submit.prevent="addTodo">
      <div class="flex items-center">
        <input v-model="newTodo" type="text"
          class="flex-1 py-1.5 pl-2 pr-7 rounded-md border border-gray-300 placeholder:text-gray-400 focus:ring-indigo-600"
          placeholder="New Task">
        <button
          class="flex-none py-1.5 px-5 rounded-md border-0 bg-indigo-600 text-white hover:bg-indigo-700 focus:outline-none focus:ring focus:ring-indigo-300 focus:bg-indigo-700">Add</button>
      </div>
    </form>
  </div>
</template>
