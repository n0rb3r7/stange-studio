<template>
  <article class="container"><nuxt-content :document="work" /></article>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const work = await $content('works', params.slug).fetch()
    return { work }
  },
}
</script>

<style>
.nuxt-content img {
  max-width: 300px;
}
</style>
