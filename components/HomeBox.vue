<script setup>
defineProps({
  infos: Object,
})
</script>

<template>
  <section
    :class="[
      infos.main ? 'main-section' : 'secondary-section',
      infos.order === 'invert' ? 'inverted' : '',
    ]">
    <div class="image" :class="infos.main ? 'main-image' : ''">
      <picture>
        <source media="(min-width: 1025px)" :srcset="infos.images.large" />
        <img :src="infos.images.small" :alt="infos.title" />
      </picture>
    </div>
    <div class="content" :class="infos.main ? 'main-content' : ''">
      <h2 class="tp-1" v-if="!infos.main">{{ infos.title }}</h2>
      <h1 class="tp-1" v-if="infos.main">{{ infos.title }}</h1>
      <p class="tp-body">
        {{ infos.body }}
      </p>
      <Button type="ternary-dark" :label="infos.btnLabel" large="false" v-if="!infos.main" />
      <Button type="ternary" :label="infos.btnLabel" large="false" v-if="infos.main" />
    </div>
  </section>
</template>

<style scoped>
section {
  --left-padding: 3rem;
  overflow-x: hidden;
}

.main-section {
  background-color: var(--black-900);
}

.content {
  padding-block: 3.5rem;
}

h1 {
  color: var(--white-900);
  max-width: 380px;
  text-transform: uppercase;
}

h2 {
  color: var(--black-900);
  max-width: 380px;
  text-transform: uppercase;
}

p {
  color: var(--grey-dark);
  margin-block: 1.5rem;
  max-width: 400px;
}

.image img {
  width: 100%;
  max-height: 620px;
  object-fit: cover;
}

@media (min-width: 1025px) {
  section {
    align-items: center;
  }
  .secondary-section {
    display: grid;
    grid-template-columns: 60% 40%;
    gap: var(--left-padding);
  }
  .main-section {
    display: grid;
    grid-template-columns: 40% 60%;
    gap: var(--left-padding);
  }

  .secondary-section.inverted {
    grid-template-columns: 40% 60%;
  }
  .secondary-section.inverted .image {
    order: 2;
  }
  .secondary-section.inverted .content {
    order: 1;
    padding-left: var(--left-padding);
  }

  .main-section.inverted {
    grid-template-columns: 60% 40%;
  }
  .main-section.inverted .image {
    order: 1;
  }
  .main-section.inverted .content {
    order: 2;
    padding-left: var(--left-padding);
  }

  .main-content {
    padding-left: var(--left-padding);
  }
  .image img {
    height: 100%;
  }
  .main-image {
    order: 2;
  }
}
</style>
