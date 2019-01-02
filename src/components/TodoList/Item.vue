<template>
    <li class="list-group-item">
            <span>
                <slot></slot>
            </span>
            <button class="btn btn-primary" type="submit">All Done!</button>
    </li>
</template>
<script>
  export default {
    name: 'item',
  };
</script>
<style>
  .list-group-item {
      display: flex !important;
      justify-content: space-between;
      align-items: center;
  }
</style>
