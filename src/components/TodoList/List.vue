<template>
    <div class="row">
        <div class="card mx-auto" >
            <ul class="list-group list-group-flush">
                <Item v-for="item in todoList"
                      v-if="!item.done"
                      v-bind:itemId="item.id"
                      v-bind:key="item.id"
                >
                    {{ item.description }}
                </Item>
            </ul>
        </div>
    </div>
</template>
<script>
import Item from './Item.vue';

export default {
  name: 'list',
  components: {
    Item
  },
  props: {
    todoList: Array
  }
};
</script>
<style scoped>
.card {
  max-width: 600px;
}
</style>
