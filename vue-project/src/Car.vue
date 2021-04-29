<template>
  <div class="car">
    <h3>Name: {{carName}}</h3>
    <p>Year: {{carYear}}</p>
    <button @click="changeName">Cange name</button>
    <button @click="changeFunc">Cange to Audi</button>
  </div>
</template>

<script>
export default {
  // props: [
  //   'carName', 'carYear'
  // ]
  props: {
    carName: {
      type: String,
      default: 'defolto'
    },
    carYear: {
      type: Number,
      required: false
    },
    changeFunc: {
      type: Function
    }
  },
  methods: {
    changeName() {
      this.carName = 'Mazda',
      this.$emit('nameChangeddd', this.carName)
    }
  }
}
</script>

<style>
.car {
  border: 1px solid black;
}
</style>
