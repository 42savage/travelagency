<template>
  <div>
    <animations />
    <navigation />
    <Nuxt />
  </div>
</template>
<script>
import animations from '~/components/animations.vue'
import navigation from '~/components/navigation.vue'
export default {
  components: {
    navigation,
    animations,
  },
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@300;400;700&display=swap');
html {
  font-family: 'Oswald', sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
</style>
