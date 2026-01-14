<script setup>
defineProps({
  values: Object,
})
</script>

<template>
  <article>
    <h3 class="tp-2">{{ values.label }}</h3>
    <p class="tp-body description">
      {{ values.text }}
    </p>
    <p>
      <strong class="tp-1">{{ values.price }}</strong>
    </p>
    <p class="tp-body">per {{ values.renewal }}</p>

    <button class="tp-4">PICK PLAN</button>
  </article>
</template>

<style scoped>
article {
  padding-inline: 2.5rem;
  padding-block: 3rem;
  background-color: var(--grey-400);
}

h3 {
  margin-bottom: 1rem;
}

.description {
  margin-bottom: 2rem;
}

h3,
p {
  text-align: center;
}

p {
  color: var(--grey-dark);
}

strong {
  color: var(--black-900);
}

button {
  border: none;
  cursor: pointer;
  display: block;
  width: 100%;
  max-width: 450px;
  margin-inline: auto;
  padding-block: 0.9rem;
  margin-top: 2rem;
  background-color: var(--black-900);
  color: var(--white-900);
}
</style>
