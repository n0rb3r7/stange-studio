<template>
  <b-navbar>
    <template #brand>
      <b-navbar-item tag="router-link" :to="{ path: '/' }">
        <StangeStudioLogo :height="35" :width="35" />
      </b-navbar-item>
    </template>
    <template #end>
      <b-navbar-item v-for="(item, key) of items" :key="key">
        <NuxtLink :to="item.to" exact-active-class="is-active">
          <span>{{ item.title }}</span>
        </NuxtLink>
      </b-navbar-item>
      <b-navbar-item>
        <div class="buttons">
          <NuxtLink class="button is-danger" to="/contact">
            <strong>Contacto</strong>
          </NuxtLink>
        </div>
      </b-navbar-item>
    </template>
  </b-navbar>
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
