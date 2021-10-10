<template>
  <article class="container">
    <SocialHead
      :title="work.title"
      :description="work.description"
      :image="work.image"
    /><nuxt-content :document="work" />
  </article>
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
  max-width: 100%;
}
</style>
