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

const values = ref({
  
})
</script>

<template>
  <div>
    <main class="mx-width">
      <HomeBox :infos="datas" v-if="datas" />
      <section class="offers">
        <OfferBtn />
        <OfferCard />
      </section>
    </main>
  </div>
</template>

<style scoped></style>
