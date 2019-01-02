<template>
    <div>
        Hi! I'm the List!
        <Item></Item>
    </div>
</template>
<script>
  import Item from './Item.vue';
  export default {
    name: 'list',
    components: {
      Item,
    }
  };
</script>
<style>

</style>
