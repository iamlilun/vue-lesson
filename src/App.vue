<<script>
import TodoInput from './TodoInput.vue';
import TodoItem from './TodoItem.vue';

export default{
  components:{
    TodoInput,
    TodoItem, 
  },
  data(){
    return {
      todos: [],
    };
  },
  methods:{
    addTodo(text){
      this.todos.push(text);
    }
  }
};
</script>

<template>
  <div>
    <TodoInput @submit="addTodo" />
    <ul>
      <TodoItem v-for="todo in todos" :key='todo' :data="todo" />
    </ul>
  </div>
</template>

<style>

</style>