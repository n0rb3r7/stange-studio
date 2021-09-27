<template>
  <svg
    :fill="iconColor"
    :width="width"
    :height="height"
    viewBox="0 0 200 200"
    x="0px"
    y="0px"
  >
    <g>
      <polygon points="199,35.3 199,1 1,1 1,119.3 	" />
      <polygon points="1,162.4 1,199 199,199 199,78.3 	" />
    </g>
  </svg>
</template>

<script>
export default {
  props: {
    width: {
      type: [Number, String],
      default: 18,
    },
    height: {
      type: [Number, String],
      default: 18,
    },
    iconColor: {
      type: String,
      default: 'black',
    },
  },
}
</script>

<style></style>
