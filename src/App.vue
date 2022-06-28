<template>
  <TopBar />
  <div class="bg-gradient-to-r from-indigo-500 via-purple-500 to-pink-500">
    <router-view />
  </div>
</template>

<script>
  import TopBar from '@/components/TopBar.vue'
  export default {
    name: 'HomeView',
    components: {
      TopBar
    }
  }
</script>

<style lang="scss">
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
  }
  .container{
    padding: 3%;
  }
</style>
