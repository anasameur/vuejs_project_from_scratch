<template>
    <div class="full-width center-content">
        <hello-component name="bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb" />
    </div>
</template>

<script>
import HelloComponent from './components/HelloComponent.vue';
export default {
  components: {
    HelloComponent,
  },
};
</script>
<style scoped>
.full-width {
  width: 100%;
}
.center-content {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
