<template>
    <div class="container">
        <h1>welcome</h1>
        <Form></Form>
        <List></List>
    </div>
</template>
<script>
  import { Form, List } from '../components';
  export default {
    name: 'todo',
    components: {
      Form,
      List
    }
  };
</script>
<style>

</style>
