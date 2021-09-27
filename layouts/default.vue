<template>
  <div>
    <TheNavBar />
    <Nuxt />
    <TheFooter />
  </div>
</template>

<script>
import TheNavBar from '~/layouts/TheNavBar'
import TheFooter from '@/layouts/TheFooter.vue'

export default {
  components: {
    TheNavBar: TheNavBar,
    TheFooter: TheFooter,
  },
  data() {
    return {}
  },
}
</script>
<style>
body {
  background-color: rgb(228, 228, 228);
  min-height: 100vh;
}

p:last-of-type {
  margin-bottom: 0px;
}
</style>
