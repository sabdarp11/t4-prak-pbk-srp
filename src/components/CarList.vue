<template>
  <div>
    <h2>Car List</h2>
    <CarItem v-for="car in cars" :key="car.id" :car="car" @car-selected="showCarDetail" />
  </div>
</template>

<script>
import CarItem from './CarItem.vue'

export default {
  name: 'CarList',
  components: {
    CarItem
  },
  data() {
    return {
      cars: [
        {
          id: 1,
          name: 'Toyota',
          model: 'Supra MK4',
          image: 'https://link-to-toyota-supra-image.com'
        },
        { id: 2, name: 'Honda', model: 'Civic', image: 'https://link-to-honda-civic-image.com' },
        { id: 3, name: 'BMW', model: 'M4 Competition', image: 'https://link-to-bmw-m4-image.com' }
      ]
    }
  },
  methods: {
    showCarDetail(car) {
      this.$emit('car-detail', car)
    }
  }
}
</script>

<style scoped>
h2 {
  margin-bottom: 20px;
}
</style>
