<template>
  <div>
    <div class="navbar-fixed">
      <nav>
        <div class="nav-wrapper container">
          <NuxtLink class="brand-logo" to="/"
            ><StangeStudioLogo :height="25" :width="25" :iconColor="false"
          /></NuxtLink>
          <a href="#" data-target="sidenav" class="sidenav-trigger"
            ><i class="material-icons">menu</i></a
          >
          <ul
            v-for="(item, key) of items"
            :key="key"
            tag="router-link"
            class="right hide-on-med-and-down"
          >
            <li>
              <NuxtLink v-if="item.title !== 'Contacto'" :to="item.to">{{
                item.title
              }}</NuxtLink>
              <NuxtLink
                v-else
                :to="item.to"
                class="btn pink darken-1 waves-effect waves-light"
                >{{ item.title }}
              </NuxtLink>
            </li>
          </ul>
        </div>
      </nav>
    </div>
    <ul class="sidenav" id="sidenav">
      <StangeStudioLogo :height="35" :width="35" :iconColor="false" />
      <li v-for="(item, key) of items" :key="key" tag="router-link">
        <NuxtLink
          v-if="item.title !== 'Contacto'"
          :to="item.to"
          class="text-white waves-effect waves-light"
          >{{ item.title }}</NuxtLink
        >
      </li>
      <li>
        <NuxtLink
          to="contact"
          class="btn pink darken-1 waves-effect waves-light"
          >Contacto
        </NuxtLink>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'TheNavBar',
  data() {
    return {
      items: [
        {
          title: 'Contacto',
          to: { name: 'contact' },
        },
        {
          title: 'Works',
          to: { name: 'works' },
        },
        {
          title: 'About',
          to: { name: 'about' },
        },
        {
          title: 'Home',
          to: { name: 'index' },
        },
      ],
    }
  },
}
</script>

<style>
nav {
  background-color: rgba(14, 14, 28, 0.95);
}
.sidenav {
  background-color: rgba(14, 14, 28, 1);
  color: white;
}
.sidenav li > a {
  color: white;
}
</style>
