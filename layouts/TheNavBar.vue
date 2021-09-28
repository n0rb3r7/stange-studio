<template>
  <b-navbar>
    <template #brand>
      <b-navbar-item tag="router-link" :to="{ path: '/' }">
        <StangeStudioLogo :height="35" :width="35" />
      </b-navbar-item>
    </template>
    <template #end>
      <b-navbar-item
        v-for="(item, key) of items"
        :key="key"
        tag="router-link"
        :to="item.to"
      >
        <span>{{ item.title }}</span>
      </b-navbar-item>
      <b-navbar-item tag="router-link" to="/contact">
        <div class="button is-danger"><strong>Contacto</strong></div>
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
