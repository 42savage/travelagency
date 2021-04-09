<template></template>
<script>
export default {
  name: 'Animations',
  methods: {
    watchColors() {
      const tl = this.$gsap.timeline({
        scrollTrigger: {
          trigger: '.tour-wrapper',
          start: 'top 5%',
          end: 'top 5%',
          scrub: 1,
          delay: 0,
        },
      })
      tl.addLabel('targetPoint')
        .to(
          '.lg',
          {
            color: '#084C61',
          },
          'targetPoint'
        )
        .to(
          '.ln',
          {
            background: '#084C61',
          },
          'targetPoint'
        )
        .to('.nav-wrapper', {
          background: '#ffffff',
        })
      return tl
    },
    watchColors2() {
      const tl = this.$gsap.timeline({
        scrollTrigger: {
          trigger: '.about-wrapper',
          start: 'top 5%',
          end: 'top 5%',
          scrub: 1,
          delay: 0,
        },
      })
      tl.addLabel('targetPoint')
        .to(
          '.lg',
          {
            color: '#ffffff',
          },
          'targetPoint'
        )
        .to(
          '.ln',
          {
            background: '#ffffff',
          },
          'targetPoint'
        )
        .to('.nav-wrapper', {
          background: '#4F6D7A',
          opacity: 0.9,
        })
      return tl
    },
    watchColors3() {
      const tl = this.$gsap.timeline({
        scrollTrigger: {
          trigger: '.contact-wrapper',
          start: 'top 5%',
          end: 'top 5%',
          scrub: 1,
          delay: 0,
        },
      })
      tl.addLabel('targetPoint')
        .to(
          '.lg',
          {
            color: '#084C61',
          },
          'targetPoint'
        )
        .to(
          '.ln',
          {
            background: '#084C61',
          },
          'targetPoint'
        )
        .to('.nav-wrapper', {
          background: '#ffffff',
        })
      return tl
    },
  },
  mounted() {
    this.watchColors()
    this.watchColors2()
    this.watchColors3()
  },
}
</script>
