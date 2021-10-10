<template>
  <footer class="page-footer">
    <div class="container">
      <div class="row">
        <div class="col l6 s12">
          <h5 class="white-text">Footer Content</h5>
          <p class="grey-text text-lighten-4">
            You can use rows and columns here to organize your footer content.
          </p>
        </div>
        <div class="col l4 offset-l2 s12">
          <h5 class="white-text">Links</h5>
        </div>
      </div>
    </div>
    <div class="footer-copyright">
      <div class="container">
        © {{ currentDate.getFullYear() }} Stange Studio
        <a
          class="grey-text text-lighten-4 right"
          target="_blank"
          rel="noopener noreferrer"
          href="https://nuxtjs.org"
          >Made with NuxtJS</a
        >
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'TheFooter',
  data() {
    return {
      currentDate: new Date(),
    }
  },
}
</script>

<style>
.page-footer {
  background-color: rgba(14, 14, 28, 0.95);
  flex: 0;
}
</style>
