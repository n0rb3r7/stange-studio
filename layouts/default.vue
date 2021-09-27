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
