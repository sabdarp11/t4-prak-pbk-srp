<template>
  <div id="app">
    <CarList @car-detail="displayCarDetail" />
    <CarDetail :car="selectedCar">
      <template v-slot:default>
        <p><em>Additional information about the car can go here.</em></p>
      </template>
    </CarDetail>
  </div>
</template>

<script>
import CarList from './components/CarList.vue'
import CarDetail from './components/CarDetail.vue'

export default {
  name: 'App',
  components: {
    CarList,
    CarDetail
  },
  data() {
    return {
      selectedCar: null
    }
  },
  methods: {
    displayCarDetail(car) {
      this.selectedCar = car
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
