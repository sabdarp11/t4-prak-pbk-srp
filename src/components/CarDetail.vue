<template>
  <div v-if="car">
    <h2>Car Detail</h2>
    <p><strong>Name:</strong> {{ car.name }}</p>
    <p><strong>Model:</strong> {{ car.model }}</p>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'CarDetail',
  props: {
    car: Object
  }
}
</script>

<style scoped>
div {
  border: 1px solid #ccc;
  padding: 20px;
  margin-top: 20px;
}
</style>
