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
</script>

<template>
  <div>
    <main class="mx-width">
      <HomeBox :infos="datas" v-if="datas" />
    </main>
  </div>
</template>

<style scoped></style>
