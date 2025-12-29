<script setup>
const carouselData = ref({
  1: {
    imgs: ['/images/stories/desktop/mountains.jpg', '/images/stories/mobile/mountains.jpg'],
    label: 'The Mountains',
    author: 'John Appleseed',
    date: 'April 16th 2021',
    dateTime: '2021-04-16',
  },
  2: {
    imgs: ['/images/stories/desktop/cityscapes.jpg', '/images/stories/mobile/cityscapes.jpg'],
    label: 'Sunset Cityscapes',
    author: 'Benjamin Cruz',
    date: 'September 23rd 2022',
    dateTime: '2022-09-23',
  },
  3: {
    imgs: [
      '/images/stories/desktop/18-days-voyage.jpg',
      '/images/stories/mobile/18-days-voyage.jpg',
    ],
    label: '18 Days Voyage',
    author: 'Alexei Borodin',
    date: 'July 12th 2023',
    dateTime: '2023-07-12',
  },
  4: {
    imgs: [
      '/images/stories/desktop/architecturals.jpg',
      '/images/stories/mobile/architecturals.jpg',
    ],
    label: 'Architecturals',
    author: 'Samantha Brooke',
    date: 'January 8th 2024',
    dateTime: '2024-01-08',
  },
  5: {
    imgs: ['/images/stories/desktop/world-tour.jpg', '/images/stories/mobile/world-tour.jpg'],
    label: 'World Tour 2019',
    author: 'by Timothy Wagner',
    date: 'November 2nd 2020',
    dateTime: '2020-11-02',
  },
  6: {
    imgs: [
      '/images/stories/desktop/unforeseen-corners.jpg',
      '/images/stories/mobile/unforeseen-corners.jpg',
    ],
    label: 'Unforeseen Corners',
    author: 'by William Malcolm',
    date: 'May 21st 2022',
    dateTime: '2022-05-21',
  },
  7: {
    imgs: [
      '/images/stories/desktop/king-on-africa.jpg',
      '/images/stories/mobile/king-on-africa.jpg',
    ],
    label: 'King on Africa: Part II',
    author: 'by Tim Hillenburg',
    date: 'March 14th 2023',
    dateTime: '2023-03-14',
  },
  8: {
    imgs: [
      '/images/stories/desktop/trip-to-nowhere.jpg',
      '/images/stories/mobile/trip-to-nowhere.jpg',
    ],
    label: 'The Trip to Nowhere',
    author: 'by Felicia Rourke',
    date: 'August 30th 2021',
    dateTime: '2021-08-30',
  },
  9: {
    imgs: [
      '/images/stories/desktop/rage-of-the-sea.jpg',
      '/images/stories/mobile/rage-of-the-sea.jpg',
    ],
    label: 'Rage of The Sea',
    author: 'by Mohammed Abdul',
    date: 'December 17th 2024',
    dateTime: '2024-12-17',
  },
  10: {
    imgs: ['/images/stories/desktop/running-free.jpg', '/images/stories/mobile/running-free.jpg'],
    label: 'Running Free',
    author: 'by Michelle',
    date: 'June 5th 2020',
    dateTime: '2020-06-05',
  },
  11: {
    imgs: [
      '/images/stories/desktop/behind-the-waves.jpg',
      '/images/stories/mobile/behind-the-waves.jpg',
    ],
    label: 'Behind the Waves',
    author: 'by Lamarr Wilson',
    date: 'February 28th 2023',
    dateTime: '2023-02-28',
  },
  12: {
    imgs: ['/images/stories/desktop/calm-waters.jpg', '/images/stories/mobile/calm-waters.jpg'],
    label: 'Calm Waters',
    author: 'by Samantha Brooke',
    date: 'October 11th 2022',
    dateTime: '2022-10-11',
  },
  13: {
    imgs: ['/images/stories/desktop/milky-way.jpg', '/images/stories/mobile/milky-way.jpg'],
    label: 'The Milky Way',
    author: 'by Benjamin Cruz',
    date: 'April 3rd 2025',
    dateTime: '2025-04-03',
  },
  14: {
    imgs: ['/images/stories/desktop/dark-forest.jpg', '/images/stories/mobile/dark-forest.jpg'],
    label: 'Night at The Dark Forest',
    author: 'by  Mohammed Abdul',
    date: 'July 19th 2021',
    dateTime: '2021-07-19',
  },
  15: {
    imgs: ['/images/stories/desktop/somwarpet.jpg', '/images/stories/mobile/somwarpet.jpg'],
    label: `Somwarpet's Beauty`,
    author: 'by Michelle',
    date: 'January 25th 2024',
    dateTime: '2024-01-25',
  },
  16: {
    imgs: [
      '/images/stories/desktop/land-of-dreams.jpg',
      '/images/stories/mobile/land-of-dreams.jpg',
    ],
    label: 'Land of Dreams',
    author: 'by William Malcolm',
    date: 'September 7th 2020',
    dateTime: '2020-09-07',
  },
})
</script>

<template>
  <div>
    <main class="">
      <StoriesHero />
      <Carousel :carousel="carouselData" />
    </main>
    <Footer />
  </div>
</template>

<style scoped></style>
