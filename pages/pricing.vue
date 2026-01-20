<script setup>
const datas = ref({
  title: 'PRICING',
  body: 'Create a your stories, Photosnap is a platform for photographers and visual storytellers. It’s the simple way to create and share your photos.',
  images: {
    large: '/images/pricing/desktop/hero.jpg',
    small: '/images/pricing/mobile/hero.jpg',
  },
  other: true,
})

const cards = ref({
  1: {
    label: 'Basic',
    text: 'Includes basic usage of our platform. Recommended for new and aspiring photographers.',
    prices: [19.00, 190.00],
    durations: ['month', 'year']
  },
  2: {
    label: 'Pro',
    text: 'More advanced features available. Recommended for photography veterans and professionals.',
    prices: [39.00, 390.00],
    durations: ['month', 'year'],
    main: true,
  },
  3: {
    label: 'Business',
    text: 'Additional features available such as more detailed metrics. Recommended for business owners.',
    prices: [99.00, 999.00],
    durations: ['month', 'year']
  }
})

const selectedPeriod = ref('month')

const handlePeriodChange = (period) => {
  selectedPeriod.value = period
}

</script>

<template>
  <div>
    <main class="mx-width">
      <HomeBox :infos="datas" v-if="datas" />
      <section class="offers">
        <OfferBtn @period-change="handlePeriodChange" />
        <div class="offers-container">
          <OfferCard v-for="card in cards" :key="card.label" :card="card" :period="selectedPeriod" />
        </div>
      </section>
    </main>
  </div>
</template>

<style scoped>
.offers-container {
  display: flex;
  gap: 2rem;
  margin-bottom: 3rem;
  align-items: flex-start
}

@media (max-width: 1024px) {
  .offers-container {
    flex-direction: column;
    align-items: center;
  }
}
</style>
