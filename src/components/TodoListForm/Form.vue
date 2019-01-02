<template>
    <form>
        <div class="form-group row">
            <input type="text" class="form-control" id="newTask" :placeholder="inputVal">
            <button type="submit" class="btn btn-primary">Add Task</button>
        </div>
    </form>
</template>
<script>
  export default {
    name: 'form',
    data() {
      return {
        inputVal: 'Enter a New Task'
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
