<template>
  <div @click="selectCar">
    <h3>{{ car.name }}</h3>
    <p>{{ car.model }}</p>
  </div>
</template>

<script>
export default {
  name: 'CarItem',
  props: {
    car: Object
  },
  methods: {
    selectCar() {
      this.$emit('car-selected', this.car)
    }
  }
}
</script>

<style scoped>
div {
  border: 1px solid #ccc;
  padding: 10px;
  margin: 10px;
  cursor: pointer;
}
</style>
