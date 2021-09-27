<template>
  <div>
    <b-navbar>
      <template #brand>
        <b-navbar-item tag="router-link" :to="{ path: '/' }">
          <img
            src="https://raw.githubusercontent.com/buefy/buefy/dev/static/img/buefy-logo.png"
            alt="Lightweight UI components for Vue.js based on Bulma"
          />
        </b-navbar-item>
      </template>
      <template #end>
        <b-navbar-item v-for="(item, key) of items" :key="key">
          <NuxtLink :to="item.to" exact-active-class="is-active">
            <b-icon :icon="item.icon" /> {{ item.title }}
          </NuxtLink>
        </b-navbar-item>
        <b-navbar-item tag="div">
          <div class="buttons">
            <NuxtLink class="button is-primary" to="/contact">
              <strong>Contacto</strong>
            </NuxtLink>
          </div>
        </b-navbar-item>
      </template>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: 'TheNavBar',
  data() {
    return {
      items: [
        {
          title: 'Home',
          to: { name: 'index' },
        },
        {
          title: 'About',
          to: { name: 'about' },
        },
        {
          title: 'Works',
          to: { name: 'works' },
        },
      ],
    }
  },
}
</script>
