<template>
    <div class="row">
        <div class="card mx-auto" >
            <ul class="list-group list-group-flush">
                <Item v-for="item in todolist">{{ item }}</Item>
            </ul>
        </div>
    </div>
</template>
<script>
  import Item from './Item.vue';
  export default {
    name: 'list',
    components: {
      Item,
    },
    data() {
      return {
        todolist: [
          'Hey Ma! I\'m Still an Item!',
          'another item',
          'oh boy!'
        ]
      }
    }
  };
</script>
<style>
    .card {
        max-width: 600px;
    }
</style>
