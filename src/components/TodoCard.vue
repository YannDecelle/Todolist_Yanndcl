<template>
    <div class="todo-card">
        <todo-header></todo-header>
        <div class="todoContainer">
            <new-todo></new-todo>
            <todo-list></todo-list>
        </div>
    </div>
</template>

<script>
import TodoList from './TodoList.vue';
import NewTodo from './NewTodo.vue';
import TodoHeader from './TodoHeader.vue';
export default {
  name: 'todo-card',
  components:{TodoList, NewTodo, TodoHeader},
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  .todo-card
  {
    background: white;
    width: 80%;
    border-radius: 40px;
  }

</style>
