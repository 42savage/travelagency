<template>
  <div class="about-wrapper">
    <h1 class="title">About us</h1>
    <div class="content">
      <div
        v-for="paragraph in paragraphs"
        :key="paragraph.id"
        class="single-paragraph"
      >
        <h3 class="paragraph-title">{{ paragraph.title }}</h3>
        <p class="paragraph-content">{{ paragraph.content }}</p>
        <a class="paragraph-link" href="#">Read more</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      paragraphs: [
        {
          id: 0,
          title: 'We are generic travel agency',
          content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam',
        },
        {
          id: 1,
          title: 'We have 10+ years of experience',
          content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam',
        },
        {
          id: 2,
          title: 'Consultant services on the best level',
          content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam',
        },
      ],
    }
  },
}
</script>

<style scoped lang="scss">
.about-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin-top: 36px;
  background: linear-gradient(
      0deg,
      rgba(79, 109, 122, 0.91),
      rgba(79, 109, 122, 0.91)
    ),
    url('~/assets/bg.jpg');
  background-size: cover;
  background-position: center;
  width: 100%;
  height: 100%;
}
.title {
  font-size: 24px;
  position: relative;
  color: white;
  font-weight: 500;
  margin-bottom: 48px;
  margin-top: 80px;
  &::after {
    content: '';
    position: absolute;
    bottom: -18px;
    left: 50%;
    transform: translate(-50%, 0);
    height: 5px;
    width: 80px;
    background: white;
  }
}
.single-paragraph {
  width: 200px;
  text-align: left;
  margin: 24px 0;
}
.paragraph-title {
  font-size: 24px;
  color: white;
  line-height: 20px;
  font-weight: 500;
}
.paragraph-content {
  font-size: 14px;
  color: white;
  margin: 12px 0;
  font-weight: 300;
}
.paragraph-link {
  color: white;
  text-decoration: underline;
}
.content {
  width: 100%;
  padding: 18px;
}
</style>
