<template>
  <div class="heading-wrapper">
    <h1 class="title">
      {{ title_first }} <span>{{ title_second }}</span>
    </h1>
    <h5 class="subtitle">{{ subtitle }}</h5>
  </div>
</template>

<script>
export default {
  props: {
    title_first: {
      type: String,
      default: '',
    },
    title_second: {
      type: String,
      default: '',
    },
    subtitle: {
      type: String,
      default: '',
    },
  },
}
</script>

<style scoped lang="scss">
.title {
  color: #084c61;
  font-size: 24px;
  position: relative;
  font-weight: 500;
  margin-top: 60px;
  span {
    color: #db504a;
  }
  &::after {
    content: '';
    position: absolute;
    bottom: -18px;
    left: 50%;
    transform: translate(-50%, 0);
    height: 5px;
    width: 80px;
    background: #db504a;
  }
}
.subtitle {
  color: #858585;
  font-size: 16px;
  font-weight: 300;
  margin-top: 32px;
}
</style>
