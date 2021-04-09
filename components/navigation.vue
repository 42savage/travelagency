<template>
  <div class="nav-wrapper">
    <nav>
      <div class="logo">
        <h3 class="lg"><b>Generic</b>Travel</h3>
        <p class="lg">agency</p>
      </div>
      <button>
        <div class="ln"></div>
        <div class="ln"></div>
        <div class="ln"></div>
      </button>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Navigation',
}
</script>

<style scoped lang="scss">
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
  align-items: center;
  padding: 18px;
  h3 {
    font-size: 24px;
  }
  h3,
  p {
    color: white;
    font-weight: 300;
  }
  p {
    text-align: right;
    line-height: 5px;
    font-size: 18px;
  }
  button {
    background: none;
    border: none;
    div {
      background: white;
      width: 36px;
      height: 3px;
      margin: 6px 0;
      &:nth-child(1) {
        width: 30px;
      }
    }
  }
}
</style>
