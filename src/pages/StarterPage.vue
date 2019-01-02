<template>
    <div class="starter-page container">
        <div class="section text-center">
            <h3>Create your next awesome website hey</h3>
        </div>
        <Card type="default" title="carlos">
            <div slot="info">test</div>
        </Card>
    </div>
</template>
<script>
    import { Card } from '../components';

    export default {
      name: 'starter',
      components: {
        Card,
      }
    };
</script>
<style>
    .starter-page {
        min-height: calc(100vh - 95px);
    }
</style>
