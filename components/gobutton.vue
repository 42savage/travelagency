<template>
  <div class="button-wrapper">
    <a :href="href">{{ title }}<arrow :transform="'rotate(180)'" /></a>
  </div>
</template>

<script>
import arrow from '~/components/icons/prevnext'
export default {
  props: {
    title: {
      type: String,
      default: 'Hello world',
    },
    href: {
      type: String,
      default: '#',
    },
  },
  components: {
    arrow,
  },
}
</script>

<style scoped lang="scss">
.button-wrapper {
  display: flex;
  justify-content: flex-end;
  width: 100%;
  padding: 0 18px;
}
a {
  background: #4f6d7a;
  text-align: center;
  color: white;
  text-decoration: none;
  transition: 0.3s;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 6px 12px;
  font-weight: 300;
  &:hover {
    text-decoration: none;
    background: #084c61;
  }
}
</style>
