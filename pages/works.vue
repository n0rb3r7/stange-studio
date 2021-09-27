<template>
  <div class="container">
    <h1>Trabajos</h1>
    <div class="works">
      <div class="work" v-for="work of works" :key="work.slug">
        <nuxt-link :to="{ name: 'work-slug', params: { slug: work.slug } }">
          <div class="work-inner">
            <img :src="require(`~/assets/works-img/${work.img}`)" alt="" />
            <div class="detail">
              <h3>{{ work.title }}</h3>
              <p>{{ work.description }}</p>
            </div>
          </div>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const works = await $content('works', params.slug)
      .only(['title', 'description', 'img', 'slug'])
      .sortBy('createdAt', 'asc')
      .fetch()
    return {
      works,
    }
  },
}
</script>

<style></style>
