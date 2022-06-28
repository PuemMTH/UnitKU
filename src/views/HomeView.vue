<template>
  <div class="home">
    <HomeDashboard />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HomeDashboard from '@/components/HomeDashboard.vue'
export default {
  name: 'HomeView',
  components: {
    HomeDashboard
  }
}
</script>
