<script setup>
defineProps({
  label: String,
  type: String,
})
</script>

<template>
  <button v-if="type == 'primary'" class="primary-btn">{{ label }}</button>
  <button v-if="type == 'secondary'" class="secondary-btn">{{ label }}</button>
</template>

<style scoped>
button {
  transition: background-color var(--time) ease-out, text-decoration-color var(--time) ease-out,
    color var(--time) ease-out;
  text-transform: uppercase;
  font-size: 12px;
  letter-spacing: 2px;
  cursor: pointer;
  width: 158px;
  height: 40px;
  border: none;
  text-align: center;
}

.primary-btn {
  background-color: var(--black-900);
  color: var(--white-900);
}

.secondary-btn {
  color: var(--black-900);
  text-decoration-color: transparent;
}

@media (hover: hover) {
  .primary-btn:hover {
    background-color: var(--grey-400);
    color: var(--black-900);
  }
  .secondary-btn:hover {
    text-decoration: underline;
    text-decoration-color: var(--black-900);
  }
}
</style>
