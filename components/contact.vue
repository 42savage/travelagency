<template>
  <div class="contact-wrapper">
    <h1 class="title">Get in touch with Us</h1>
    <p class="subtitle">
      Just give us your phone number, we will contact with you as soon as we
      can.
    </p>
    <div class="input-container">
      <input type="text" placeholder="Contact number" /><button class="sendBtn">
        Enter
      </button>
    </div>
    <div class="bottom">
      <div class="footer-logo">
        <h3><b>Generic</b>Travel</h3>
        <p>agency</p>
      </div>
      <div class="content">
        <div class="left">
          <p><phone />777-666-555</p>
          <p><phone />111-666-222</p>
          <p><email />contact@generic.co</p>
          <p><email />support@generic.co</p>
        </div>
        <div class="right">
          <pin :width="36" :height="36" />
          <div class="adress">
            <p>Poland</p>
            <p>al. Złotych Damianów</p>
            <p>22-200 Warsaw</p>
          </div>
        </div>
      </div>
      <div class="socials">
        <linkedin />
        <facebook />
        <instagram />
      </div>
    </div>
  </div>
</template>

<script>
import phone from '~/components/icons/phone-cal'
import email from '~/components/icons/email'
import facebook from '~/components/icons/facebook'
import linkedin from '~/components/icons/linkedin'
import instagram from '~/components/icons/instagram'
import pin from '~/components/icons/pin'

export default {
  name: 'contact',
  components: {
    phone,
    email,
    facebook,
    instagram,
    linkedin,
    pin,
  },
}
</script>

<style scoped lang="scss">
.contact-wrapper {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.title {
  font-size: 24px;
  color: #084c61;
  font-weight: 500;
  margin-top: 120px;
  position: relative;
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
  color: #707070;
  font-size: 14px;
  font-weight: 500;
  width: 260px;
  margin-top: 36px;
}
.input-container {
  display: flex;
  flex-direction: row;
  margin-top: 36px;
  margin-bottom: 54px;
  input {
    width: 220px;
    padding: 0 6px;
    height: 36px;
    border: 1px solid #e8e8e8;
    color: #727272;
    box-shadow: 0px 0px 8px -2px rgba(0, 0, 0, 0.25);
    border-radius: 5px;
    ::placeholder {
      color: #727272;
    }
  }
}
.sendBtn {
  border: none;
  border-radius: 0px 5px 5px 0px;
  color: white;
  background: #db504a;
  width: 42px;
  height: 36px;
  margin-left: -42px;
}
.footer-logo {
  color: white;
  width: 126px;
  margin-bottom: 36px;
  h3 {
    font-weight: 300;
    font-size: 24px;
  }
  p {
    text-align: center;
    font-size: 18px;
    line-height: 5px;
  }
}
.bottom {
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  height: 284px;
  width: 100%;
  background: linear-gradient(180deg, rgba(8, 76, 97, 0.9) 0%, #084c61 100%),
    url('~/assets/footerbg.jpg');
}
.content {
  padding: 18px;
  display: flex;
  justify-content: space-between;
  width: 100%;
}
.left,
.right {
  width: 100%;
}
.left {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  p {
    color: white;
    svg {
      margin-right: 12px;
    }
  }
}
.right {
  display: flex;
  justify-content: center;
  align-items: center;
}
.adress {
  color: white;
  text-align: left;
}
.socials {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  svg {
    margin: 0 6px;
  }
}
</style>
