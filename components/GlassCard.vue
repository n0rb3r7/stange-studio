<template>
  <div class="glassCard">
    <h5>titulo</h5>
    <p>asdada</p>
  </div>
</template>

<script>
export default {}
</script>

<style>
.glassCard {
  box-shadow: 0 0 1rem 0 rgba(0, 0, 0, 0.2);
  border-radius: 5px;
  position: relative;
  z-index: 1;
  background: inherit;
  overflow: hidden;
}

.glassCard:before {
  content: '';
  position: absolute;
  background: inherit;
  z-index: -1;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  box-shadow: inset 0 0 2000px rgba(255, 255, 255, 0.5);
  filter: blur(10px);
  margin: -20px;
}
</style>
