<template>
  <div>
    <TheNavBar />
    <Nuxt />
    <TheFooter />
  </div>
</template>

<script>
import TheNavBar from '@/layouts/TheNavBar'
import TheFooter from '@/layouts/TheFooter'

export default {
  components: {
    TheNavBar: TheNavBar,
    TheFooter: TheFooter,
  },
  data() {
    return {}
  },
  mounted() {
    M.AutoInit()
  },
}
</script>
<style>
html,
body {
  background-color: #212038;
  /* background: url(https://images.pexels.com/photos/2471234/pexels-photo-2471234.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940) */
  /* no-repeat; */
  /* Keep the inherited background full size. */
  background-attachment: fixed;
  background-size: cover;
  color: white;
  /* min-height: 100vh; */
  margin: 0;
}

a:hover {
  color: hsl(238, 34%, 84%);
}
p:last-of-type {
  margin-bottom: 0px;
}
.btn {
  border-radius: 25px !important;
}
</style>
