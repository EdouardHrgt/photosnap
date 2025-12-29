<script setup></script>

<template>
  <section class="">
    <picture class="image">
      <source
        media="(min-width: 1025px)"
        srcset="/public/images/stories/desktop/moon-of-appalacia.jpg" />

      <source
        media="(min-width: 851px)"
        srcset="/public/images/stories/tablet/moon-of-appalacia.jpg" />

      <img src="/public/images/stories/mobile/moon-of-appalacia.jpg" alt="moon of appalacia" />
    </picture>

    <div class="content">
      <strong class="tp-4 sub-title">LAST MONTH’S FEATURED STORY</strong>
      <h1 class="tp-1">HAZY FULL MOON OF APPALACHIA</h1>
      <div class="author">
        <time datetime="2025-03-12" class="tp-4">March 2nd 2025</time>
        <cite class="tp-4">by John Appleseed </cite>
      </div>
      <p class="tp-body">
        The dissected plateau area, while not actually made up of geological mountains, is popularly
        called "mountains," especially in eastern Kentucky and West Virginia, and while the ridges
        are not high, the terrain is extremely rugged.
      </p>
      <div class="wrap__btn"><Button type="ternary" label="read the story" large="true" /></div>
    </div>
  </section>
</template>

<style scoped>
.image {
  width: 100%;
}

.image img {
  width: inherit;
  object-fit: cover;
}

.content {
  background-color: var(--black-900);
  padding-inline: 1rem;
  padding-block: 2rem;
}

strong,
h1 {
  color: var(--white-900);
}

p,
time {
  color: var(--grey-dark);
}

h1 {
  margin-block: 1rem 2.5rem;
}

.author {
  margin-bottom: 1rem;
  text-transform: uppercase;
}

cite {
  margin-left: 12px;
  color: var(--grey-400);
}

.wrap__btn {
  margin-top: 1rem;
}

@media (min-width: 1025px) {
}
</style>
