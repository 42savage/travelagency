<template>
  <svg
    :transform="transform"
    fill="none"
    :width="width"
    :height="height"
    viewBox="0 0 18 30"
  >
    <path d="M16 28L3 15L16 2" :stroke="fill" stroke-width="3" />
  </svg>
</template>

<script>
export default {
  props: {
    width: {
      type: Number,
      default: 18,
    },
    height: {
      type: Number,
      default: 18,
    },
    fill: {
      type: String,
      default: 'white',
    },
    transform: {
      type: String,
      default: 'rotate(0)',
    },
  },
}
</script>

<style></style>
