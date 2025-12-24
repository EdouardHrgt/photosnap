<script setup>
const carousel = ref({
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

<template>
  <section>
    <div class="card" v-for="card in carousel" :key="card.author">
      <picture>
        <source :srcset="card.imgs[0]" media="(min-width: 400px)" />
        <img :src="card.imgs[1]" :alt="card.label" />
      </picture>
      <div class="content">
        <div class="content__text">
          <h3 class="tp-3">{{ card.label }}</h3>
          <p class="tp-4">{{ card.author }}</p>
        </div>
        <div class="wrap__btn"><Button type="ternary" label="read story" large="true" /></div>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {

}

.card {
  position: relative;
  isolation: isolate;
  width: 100%;
  aspect-ratio: 1;
}

picture {
  width: 100%;
  height: 100%;
  display: block;
}

picture::after {
  content: '';
  background-color: rgba(0, 0, 0, 0.2);
  position: absolute;
  inset: 0;
  z-index: 1;
}

picture img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

h3,
p {
  color: var(--white-900);
}

h3 {
  margin-bottom: 0.3rem;
}

.content {
  padding-inline: 1.75rem;
  position: absolute;
  bottom: 0.75rem;
  left: 0;
  right: 0;
  z-index: 5;
}

.content__text {
  border-bottom: 3px solid var(--grey-400);
  padding-bottom: 0.75rem;
}

@media (min-width: 1025px) {
  section {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(360px, 1fr));
  }
  .card {
    aspect-ratio: 1/1.3;
  }
}
</style>
