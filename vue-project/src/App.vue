<template>
  <div>
    <h1>Parent: {{ carName }}</h1>
    <app-car></app-car>
  </div>
</template>

<script>
import Car from './Car.vue'

export default {
  data () {
    return {
      carName: 'Ford from parent'
    }
  },
  components: {
    appCar: Car
  }
}
</script>

<style>

</style>
