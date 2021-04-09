<template>
  <div class="tour-wrapper">
    <h1 class="heading-title">Featured <span>tours</span></h1>
    <div class="featured-tours">
      <div v-for="tour in tours" :key="tour.id" class="single-tour">
        <div
          class="top"
          :style="{
            backgroundImage:
              'url(' + require('~/assets/' + tour.image + '.jpg') + ')',
          }"
        >
          <p class="price">${{ tour.price }}</p>
        </div>
        <div class="bottom flex">
          <p class="title">
            {{ tour.title }}
          </p>
          <p class="time">
            <calendar :fill="'DB504A'" :width="18" />
            {{ tour.time }}
          </p>
          <p class="travel">
            <plane :transform="'rotate(32)'" :fill="'#DB504A'" />
            {{ tour.travel }}
          </p>
          <p class="meal">
            <fork :fill="'#DB504A'" />
            {{ tour.meal }}
          </p>
          <p class="people">
            <user :fill="'#DB504A'" />
            {{ tour.people }}
          </p>
        </div>
      </div>
    </div>
    <gobutton :title="'Check all tours'" />
    <div class="companies">
      <h2>We have on board top airlane companies</h2>
      <div class="wrapper">
        <div class="single-company"><img src="~/assets/lot.png" /></div>
        <div class="single-company"><img src="~/assets/airfrance.png" /></div>
        <div class="single-company"><img src="~/assets/ryanair.png" /></div>
      </div>
    </div>
  </div>
</template>

<script>
import calendar from '~/components/icons/calendar'
import plane from '~/components/icons/plane'
import fork from '~/components/icons/fork'
import user from '~/components/icons/user'
import arrow from '~/components/icons/prevnext'

import gobutton from '~/components/gobutton.vue'

export default {
  name: 'Tours',
  data() {
    return {
      tours: [
        {
          id: 0,
          price: '6000',
          title: 'Grand Central Babaluba Hotel',
          time: 'from 30.05.2021 to 12.06.2021',
          travel: '30.05.2021, 16:00',
          meal: '3 per day',
          people: '3-6 people',
          image: 'hotel/babaluba',
        },
        {
          id: 1,
          price: '4000',
          title: 'Servizii’Dell Hotel Monako',
          time: 'from 12.06.2021 to 12.07.2021',
          travel: '11.06.2021, 9:00',
          meal: '3 per day',
          people: '3 people',
          image: 'hotel/monako',
        },
        {
          id: 2,
          price: '12000',
          title: '  Damianello Hotel Kobylany',
          time: 'from 12.06.2021 to 12.07.2021',
          travel: '11.06.2021, 19:00',
          meal: '3 per day',
          people: '4-6 people',
          image: 'hotel/kobylany',
        },
      ],
    }
  },
  components: {
    gobutton,
    plane,
    fork,
    user,
    calendar,
    arrow,
    calendar,
  },
}
</script>

<style scoped lang="scss">
.tour-wrapper {
  width: 100%;
}
.heading-title {
  color: #084c61;
  font-size: 24px;
  position: relative;
  font-weight: 500;
  margin-top: 100px;
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
.featured-tours {
  display: flex;
  flex-direction: row;
  overflow: hidden;
  margin-left: 36px;
  padding: 36px 0;
}
.single-tour {
  flex-shrink: 0;
  width: 222px;
  height: 306px;
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
.icon {
  img {
    width: 14px;
    height: 14px;
    margin-right: 12px;
  }
}
.plane {
  transform: rotate(32.74deg);
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
.checkBtn {
  border: none;
  color: white;
  background: #4f6d7a;
  border-radius: 3px;
  width: 120px;
  height: 24px;
  display: flex;
  justify-content: center;
  align-items: center;
  img {
    width: 7px;
    height: 13px;
    transform: rotate(180deg);
    margin-left: 6px;
  }
}
.companies {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 36px;
  h2 {
    font-size: 18px;
    color: #db504a;
    font-weight: 500;
    margin-bottom: 18px;
  }
}
.wrapper {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.single-company {
  background: #f3f3f3;
  box-shadow: 0px 0px 8px -3px rgba(0, 0, 0, 0.25);
  width: 80px;
  height: 40px;
  margin: 0 12px;
}
</style>
