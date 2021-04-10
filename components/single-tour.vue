<template>
  <div class="single-tour">
    <div
      class="top"
      :style="{
        backgroundImage: 'url(' + require('~/assets/' + image + '.jpg') + ')',
      }"
    >
      <p class="price">${{ price }}</p>
    </div>
    <div class="bottom flex">
      <p class="title">
        {{ title }}
      </p>
      <p class="time">
        <calendar :fill="'DB504A'" :width="18" />
        {{ time }}
      </p>
      <p class="travel">
        <plane :transform="'rotate(32)'" :fill="'#DB504A'" />
        {{ travel }}
      </p>
      <p class="meal">
        <fork :fill="'#DB504A'" />
        {{ meal }}
      </p>
      <p class="people">
        <user :fill="'#DB504A'" />
        {{ people }}
      </p>
    </div>
  </div>
</template>

<script>
import calendar from '~/components/icons/calendar'
import plane from '~/components/icons/plane'
import fork from '~/components/icons/fork'
import user from '~/components/icons/user'
export default {
  props: {
    title: {
      type: String,
    },
    time: {
      type: String,
    },
    title: {
      travel: String,
    },
    meal: {
      type: String,
    },
    people: {
      type: String,
    },
    image: {
      type: String,
    },
    travel: {
      type: String,
    },
    price: {
      type: String,
    },
  },
  components: {
    plane,
    fork,
    user,
    calendar,
    calendar,
  },
}
</script>

<style scoped lang="scss">
.single-tour {
  flex-shrink: 0;
  width: 222px;
  height: 316px;
  border-radius: 8px;
  box-shadow: 0px 0px 16px -4px rgba(0, 0, 0, 0.25);
  margin: 0 9px;
  background: #fcfcfc;
}
.top {
  width: 100%;
  height: 180px;
  position: relative;
}
.bottom {
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  padding: 12px 18px;
  p {
    text-align: left;
  }
}
.price {
  position: absolute;
  bottom: 0;
  right: 0;
  background: white;
  color: #e3b505;
  width: 72px;
  height: 24px;
  font-size: 14px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.title {
  font-size: 16px;
  color: #084c61;
}
.time,
.travel,
.meal,
.people {
  color: #4f6d7a;
  font-size: 12px;
}
</style>
