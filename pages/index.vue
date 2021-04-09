<template>
  <div class="container">
    <carousel />
    <tours />
    <guides />
    <about />
    <contact />
  </div>
</template>

<script>
import carousel from '@/components/carousel.vue'
import tours from '@/components/tours.vue'
import guides from '@/components/guides.vue'
import about from '@/components/aboutus.vue'
import contact from '@/components/contact.vue'
export default {
  components: {
    carousel,
    tours,
    guides,
    about,
    contact,
  },
}
</script>

<style>
* {
  box-sizing: border-box;
}
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  flex-direction: column;
}
</style>
