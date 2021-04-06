<template>
  <div class="carousel-wrapper">
    <div
      class="single-slide"
      v-for="slide in slides"
      :key="slide.id"
      :style="{
        backgroundImage:
          'url(' + require('~/assets/' + slide.image + '.jpg') + ')',
      }"
    >
      <h3>{{ slide.title }}</h3>
      <p>{{ slide.subTitle }}</p>
      <p>{{ slide.text }}</p>
      <button class="button">explore</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slides: [
        {
          id: 0,
          title: 'Greece',
          subTitle: 'Babaluba cape',
          text: 'One of the best places in europe',
          image: 'background',
        },
        {
          id: 1,
          title: 'Rome',
          subTitle: 'The Colloseum',
          text: 'An oval amphitheatre in the centre of the city of Rome',
          image: 'background2',
        },
        {
          id: 2,
          title: 'Rejkiawik',
          subTitle: 'Visit The Iceland',
          text: 'Nordic island country in the North Atlantic Ocean',
          image: 'background3',
        },
      ],
    }
  },
}
</script>

<style scoped lang="scss">
.single-slide {
  width: 100vw;
  height: 100vh;
  background-size: cover;
  background-position: center;
}
</style>
