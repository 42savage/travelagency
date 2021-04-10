<template>
  <div
    class="nav-wrapper"
    :class="{ opc: menuState }"
    v-scroll-lock="menuState"
  >
    <nav :class="{ show: menuState }">
      <div class="logo">
        <h3 class="lg"><b>Generic</b>Travel</h3>
        <p class="lg">agency</p>
      </div>
      <button @click="changeState">
        <div class="test">
          <div class="ln"></div>
          <div class="ln"></div>
          <div class="ln"></div>
        </div>
      </button>
      <div class="nav-items" v-if="menuState">
        <a href="#" class="single-link">Tours</a>
        <a href="#" class="single-link">Guides</a>
        <a href="#" class="single-link">About Us</a>
        <a href="#" class="single-link">Contact</a>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Navigation',
  data() {
    return {
      menuState: false,
    }
  },
  methods: {
    changeState() {
      this.menuState = !this.menuState
    },
  },
}
</script>

<style lang="scss">
.opc {
  opacity: 1 !important;
}

.show {
  width: 100vw;
  height: 100vh;
  background: white !important;
  button {
    margin: 9px 18px 0 0;
  }
  button .test {
    position: relative;
  }
  .ln {
    background: #084c61 !important;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    &:nth-child(1) {
      width: 36px;
      transform: rotate(-45deg);
    }
    &:nth-child(2) {
      display: none;
    }
    &:nth-child(3) {
      transform: rotate(45deg);
    }
  }
  .lg {
    color: #084c61 !important;
  }
}
.nav-wrapper {
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 5;
  background: none;
}
nav {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  padding: 18px;
  h3 {
    font-size: 24px;
  }
  h3,
  p {
    color: white;
    font-weight: 300;
    transition: 0.3s;
  }
  p {
    text-align: right;
    line-height: 5px;
    font-size: 18px;
  }
  button {
    background: none;
    border: none;
    outline: none;
    transition: 0.3s;
    div {
      background: white;
      transition: 0.3s;
      width: 36px;
      height: 3px;
      margin: 6px 0;
      &:nth-child(1) {
        width: 30px;
      }
    }
  }
}
.nav-items {
  position: absolute;
  top: 0;
  left: 0;
  margin: 144px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  height: 100vh;
  transition: 0.3s;
  .single-link {
    font-size: 48px;
    color: #084c61;
    text-decoration: none;
  }
}
</style>
