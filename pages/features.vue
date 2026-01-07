<script setup>
const datas = ref({
  title: 'FEATURES',
  body: 'We make sure all of our features are designed to be loved by every aspiring and even professional photograpers who wanted to share their stories.',
  images: {
    large: '/images/features/desktop/hero.jpg',
    small: '/images/features/mobile/hero.jpg',
  },
  other: true,
})
</script>

<template>
  <div>
    <main class="mx-width">
      <HomeBox :infos="datas" v-if="datas" />
    </main>
    <HomeBanner :main="true" />
    <HomeBanner :secondary="true" />
  </div>
</template>

<style scoped></style>
