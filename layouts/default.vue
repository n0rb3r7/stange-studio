<template>
  <div>
    <TheNavBar />
    <Nuxt />
  </div>
</template>

<script>
import TheNavBar from '~/layouts/TheNavBar'

export default {
  components: {
    TheNavBar: TheNavBar,
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
