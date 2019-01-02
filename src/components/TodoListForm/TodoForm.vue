<template>
    <form>
        <div class="form-group row">
            <input type="text"
                   class="form-control"
                   id="newTask"
                   :placeholder="inputVal"
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
  export default {
    name: 'todoForm',
    data() {
      return {
        inputVal: 'Enter a New Task'
      }
    },
    methods: {
      addTodo() {
        this.$emit('addTodo', this.inputVal);
        this.inputVal = 'Enter a New Task';
      }
    }
  };
</script>
<style>
    form .form-group button {
        width: 100%;
    }

    form {
        margin: 0 auto;
        max-width: 600px;
    }
</style>
