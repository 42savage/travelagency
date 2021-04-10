<template>
  <div class="single-company">
    <p><img :src="require(`../assets/${image}.png`)" /></p>
  </div>
</template>

<script>
export default {
  props: {
    image: {
      type: String,
    },
  },
}
</script>

<style scoped lang="scss">
.single-company {
  background: #f3f3f3;
  box-shadow: 0px 0px 8px -3px rgba(0, 0, 0, 0.25);
  width: 80px;
  height: 40px;
  margin: 0 12px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
