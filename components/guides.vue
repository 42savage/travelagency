<template>
  <div class="guides">
    <h1 class="title">Featured <span>guides</span></h1>
    <p class="subtitle">Guides written by best voyages in the world.</p>
    <div class="guides-wrapper">
      <div
        v-for="guide in guides"
        :key="guide.id"
        class="single-guide"
        :style="{
          backgroundImage:
            'linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, #000000 100%),' +
            'url(' +
            require('~/assets/' + guide.image + '.jpg') +
            ')',
        }"
      >
        <div class="content">
          <h3 class="guide-title">{{ guide.title }}</h3>
          <p class="guide-subtitle">{{ guide.subtitle }}</p>
          <div class="btnContainer">
            <button class="exploreBtn">Read the guide</button>
          </div>
        </div>
      </div>
    </div>
    <gobutton :title="'View more 90+ guides'" />
  </div>
</template>

<script>
import gobutton from '~/components/gobutton.vue'
export default {
  name: 'Guides',
  data() {
    return {
      guides: [
        {
          id: 0,
          title: 'Monako',
          subtitle: 'Best place in the world',
          image: 'guides/monaco',
        },
        {
          id: 1,
          title: 'Kamboja',
          subtitle: 'Best place in the world',
          image: 'guides/cambodia',
        },
        {
          id: 0,
          title: 'Rome',
          subtitle: 'Best place in the world',
          image: 'guides/rome',
        },
      ],
    }
  },
  components: {
    gobutton,
  },
}
</script>

<style scoped lang="scss">
.guides {
  width: 100%;
}
.title {
  font-size: 24px;
  color: #084c61;
  font-weight: 500;
  position: relative;
  margin-top: 80px;
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
.guides-wrapper {
  margin-top: 36px;
  display: flex;
  flex-direction: row;
  margin-left: 36px;
  overflow: hidden;
  margin-bottom: 36px;
}
.single-guide {
  width: 180px;
  height: 320px;
  box-shadow: 0px 0px 15px 1px rgba(0, 0, 0, 0.25);
  background-size: cover;
  background-position: center;
  margin: 0 16px;
  flex-shrink: 0;
  display: flex;
  justify-content: flex-end;
  align-items: flex-end;
}
.guide-title {
  font-size: 24px;
  color: white;
  font-weight: 500;
  text-align: right;
}
.guide-subtitle {
  font-size: 14px;
  color: white;
  text-align: right;
}
.exploreBtn {
  color: black;
  background: white;
  border: none;
  padding: 6px 12px;
  margin-top: 6px;
}
.btnContainer {
  width: 100%;
  display: flex;
  justify-content: flex-end;
}
.content {
  padding: 18px;
}
</style>
