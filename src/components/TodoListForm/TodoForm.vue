<template>
    <form>
        <div class="form-group row">
            <input type="text"
                   class="form-control"
                   id="newTask"
                   :placeholder="placeholder"
                   v-model="inputVal"
            >
            <button class="btn btn-primary"
                    @click="addTodo"
            >
                Add Task
            </button>
        </div>
    </form>
</template>
<script>
import { EventBus } from '../../event-bus';

export default {
  name: 'todoForm',
  data() {
    return {
      placeholder: 'Enter a New Task',
      inputVal: ''
    };
  },
  methods: {
    addTodo() {
      EventBus.$emit('addTodo', this.inputVal);
      this.inputVal = '';
    }
  }
};
</script>
<style scoped>
form .form-group button {
  width: 100%;
}

form {
  margin: 0 auto;
  max-width: 600px;
}
</style>
