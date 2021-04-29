<template>
  <div>
    <h1>Parent: {{ carName }}</h1>
    <app-car
    :carName="carName"
    :carYear="carYear"
    @nameChangeddd= "carName = $event"
    :changeFunc="changeNametoAudi"
    ></app-car>
  </div>
</template>

<script>
import Car from './Car.vue'

export default {
  data () {
    return {
      carName: 'Ford',
      carYear: 2020
    }
  },
  components: {
    appCar: Car
  },
  methods: {
    changeNametoAudi() {
      this.carName = 'Audi'
    }
  }
}
</script>

<style>

</style>
