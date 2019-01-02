<template>
    <div class="container">
        <h1>welcome</h1>
        <TodoForm></TodoForm>
        <List v-bind:todoList="todoList"></List>
    </div>
</template>
<script>
  import { TodoForm, List } from '../components';
  import { EventBus } from '../event-bus';

  export default {
    name: 'todo',
    components: {
      TodoForm,
      List
    },
    data() {
      return {
        todoList: [
          {
            id: 1,
            description: 'Hey Ma! I\'m Still an Item!',
            done: false
          },
          {
            id: 2,
            description: 'another item',
            done: false
          },
          {
            id: 3,
            description: 'oh boy!',
            done: false
          },
        ]
      }
    },
    mounted() {
      EventBus.$on('completeTask', itemId => {
        this.todoList.forEach(item => item.done = (itemId == item.id));
      });
      EventBus.$on('addTodo', newTodoDescription => {
        this.todoList.push({
          id: parseInt(new Date()),
          description: newTodoDescription,
          done: false
        });
      });
    }
  };
</script>
<style>

</style>
