<template>
  <div>
    <h1>{{ title }}</h1>

    <input type="text" v-model="searchName">
    <ul>
      <li v-for="name of filteredNames">{{ name }}</li>
    </ul>
  </div>
</template>

<script>

export default {
  data () {
    return {
      title: 'Hello i am vue',
      searchName: '',
      names: ['vlad', 'max', 'elena', 'igor']
    }
  },
  computed: {
    filteredNames() {
      return this.names.filter(name => {
        return name.toLowerCase().indexOf(this.searchName.toLowerCase()) !==-1
      })
    }
  }
}
</script>

<style>

</style>
