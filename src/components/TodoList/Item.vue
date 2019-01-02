<template>
    <li class="list-group-item">
        <span>
            <slot></slot>
        </span>
        <button class="btn btn-primary" type="submit" @click="completeTask">All Done!</button>
    </li>
</template>
<script>
  import { EventBus } from '../../event-bus';
  export default {
    name: 'item',
    methods: {
      completeTask() {
        EventBus.$emit('completeTask', this.itemId);
      }
    },
    props: {
      itemId: Number
    }
  };
</script>
<style>
  .list-group-item {
      display: flex !important;
      justify-content: space-between;
      align-items: center;
  }
</style>
