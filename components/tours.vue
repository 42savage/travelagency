<template>
  <div class="tour-wrapper">
    <heading :title_first="'Featured'" :title_second="'tours'" />
    <div class="featured-tours">
      <singleTour
        v-for="tour in tours"
        :key="tour.id"
        :image="tour.image"
        :price="tour.price"
        :title="tour.title"
        :time="tour.time"
        :travel="tour.travel"
        :meal="tour.meal"
        :people="tour.people"
      />
    </div>
    <gobutton :title="'Check all tours'" />
    <div class="companies">
      <h2>We have on board top airlane companies</h2>
      <div class="company-wrapper">
        <singleCompany
          v-for="company in companies"
          :key="company.id"
          :image="company.image"
        />
      </div>
    </div>
  </div>
</template>

<script>
import gobutton from '~/components/gobutton.vue'
import heading from '~/components/heading.vue'
import singleTour from '~/components/single-tour.vue'
import singleCompany from '~/components/single-company.vue'

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
      companies: [
        {
          id: 0,
          name: 'lot',
          image: 'lot',
        },
        {
          id: 1,
          name: 'airfrance',
          image: 'airfrance',
        },
        {
          id: 2,
          name: 'ryanair',
          image: 'ryanair',
        },
      ],
    }
  },
  components: {
    gobutton,
    heading,
    singleTour,
    singleCompany,
  },
}
</script>

<style scoped lang="scss">
.company-wrapper {
  display: flex;
  flex-direction: row;
}
.tour-wrapper {
  width: 100%;
}
.featured-tours {
  display: flex;
  flex-direction: row;
  overflow: hidden;
  margin-left: 36px;
  padding: 36px 0;
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
</style>
