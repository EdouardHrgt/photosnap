<script setup>
const datas = ref({
  1: {
    title: 'Create and share your photo stories.',
    body: 'Photosnap is a platform for photographers and visual storytellers. We make it easy to share photos, tell stories and connect with others.',
    btnLabel: 'get an invite',
    images: {
      large: '/images/home/desktop/create-and-share.jpg',
      small: '/images/home/mobile/create-and-share.jpg',
    },
    main: true,
  },
  2: {
    title: 'beautiful stories every time',
    body: 'We provide design templates to ensure your stories look terrific. Easily add photos, text, embed maps and media from other networks. Then share your story with everyone.',
    btnLabel: 'view the stories',
    order: '',
    images: {
      large: '/images/home/desktop/beautiful-stories.jpg',
      small: '/images/home/mobile/beautiful-stories.jpg',
    },
  },
  3: {
    title: 'designed for everyone',
    body: 'Photosnap can help you create stories that resonate with your audience.  Our tool is designed for photographers of all levels, brands, businesses you name it.',
    btnLabel: 'view the stories',
    order: 'invert',
    images: {
      large: '/images/home/desktop/designed-for-everyone.jpg',
      small: '/images/home/mobile/designed-for-everyone.jpg',
    },
  },
})

const carouselData = ref({
  1: {
    imgs: ['/images/stories/desktop/mountains.jpg', '/images/stories/mobile/mountains.jpg'],
    label: 'The Mountains',
    author: 'John Appleseed',
  },
  2: {
    imgs: ['/images/stories/desktop/cityscapes.jpg', '/images/stories/mobile/cityscapes.jpg'],
    label: 'Sunset Cityscapes',
    author: 'Benjamin Cruz',
  },
  3: {
    imgs: [
      '/images/stories/desktop/18-days-voyage.jpg',
      '/images/stories/mobile/18-days-voyage.jpg',
    ],
    label: '18 Days Voyage',
    author: 'Alexei Borodin',
  },
  4: {
    imgs: [
      '/images/stories/desktop/architecturals.jpg',
      '/images/stories/mobile/architecturals.jpg',
    ],
    label: 'Architecturals',
    author: 'Samantha Brooke',
  },
})
</script>
v

<template>
  <div>
    <main class="mx-width">
      <HomeBox v-for="box in datas" :key="box.title" :infos="box" v-if="datas" />
    </main>
    <Carousel :carousel="carouselData" />
    <HomeBanner />
    <Footer />
  </div>
</template>

<style scoped></style>
