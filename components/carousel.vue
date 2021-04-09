<template>
  <div class="carousel-wrapper">
    <div
      class="single-slide flex"
      v-for="slide in slides"
      :key="slide.id"
      :style="{
        backgroundImage:
          'url(' + require('~/assets/' + slide.image + '.jpg') + ')',
      }"
    >
      <h3 class="title">{{ slide.title }}</h3>
      <p class="subtitle">{{ slide.subTitle }}</p>
      <p class="text">{{ slide.text }}</p>
      <button class="exploreBtn">explore</button>
    </div>
    <div class="carousel-navigation flex">
      <div class="counter flex fc">
        <p>01/0{{ this.slides.length }}</p>
      </div>
      <div class="buttons flex fc">
        <div class="prev flex fc"><arrow /></div>
        <div class="next flex fc"><arrow :transform="'rotate(180)'" /></div>
      </div>
    </div>
  </div>
</template>

<script>
import arrow from '~/components/icons/prevnext.vue'
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
  components: {
    arrow,
  },
}
</script>

<style scoped lang="scss">
.flex {
  display: flex;
}
.fc {
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.single-slide {
  width: 100%;
  height: 100%;
  flex-shrink: 0;
  background-size: cover;
  background-position: center;
  justify-content: center;
  align-items: flex-start;
  flex-direction: column;
  padding: 18px;
}
.title,
.subtitle,
.text {
  color: white;
  font-weight: 300;
}
.title {
  font-size: 72px;
  line-height: 80px;
  margin-bottom: 6px;
}
.subtitle {
  font-size: 24px;
  line-height: 20px;
}
.text {
  font-size: 14px;
  margin-bottom: 36px;
}
.exploreBtn {
  background: white;
  border: none;
  color: black;
  width: 120px;
  height: 40px;
}
.carousel-wrapper {
  position: relative;
  display: flex;
  flex-wrap: nowrap;
  flex-direction: row;
  overflow: hidden;
  width: 100%;
  height: 100vh;
}
.carousel-navigation {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  flex-direction: row;
  justify-content: space-between;
  .buttons,
  .counter {
    flex-direction: row;
  }
  .counter {
    margin-left: 18px;
  }
  .buttons div {
    width: 60px;
    height: 60px;
    background: black;
  }
  p {
    color: white;
  }
}
</style>
