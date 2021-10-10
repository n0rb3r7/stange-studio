<template>
  <div>
    <div class="hero-image">
      <div class="glass"></div>
    </div>
    <section
      style="
        min-height: 50vh;
        background-image: url('https://images.pexels.com/photos/2471234/pexels-photo-2471234.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940');
      "
    >
      <div class="container">
        <div class="row">
          <div class="col m6"><GlassCard /></div>
          <div class="col m6"><GlassCard /></div>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
export default {
  mounted() {
    M.AutoInit()
  },
}
</script>
<style>
.hero-image {
  background-image: url('https://images.pexels.com/photos/2471234/pexels-photo-2471234.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940');
  height: calc(100vh - 64px);
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}

.hero-text {
  text-align: left;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
}
.glass {
  width: 50%;
  height: 100%;
  box-shadow: 0 0 1rem 0 rgba(0, 0, 0, 0.2);
  position: relative;
  z-index: 1;
  background: inherit;
  overflow: hidden;
  background-color: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5));
}

.glass:before {
  content: '';
  position: absolute;
  background: inherit;
  background-color: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5));

  z-index: -1;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  box-shadow: inset 0 0 2000px rgba(255, 255, 255, 0.9);
  filter: blur(10px);
  margin: -20px;
}
</style>
