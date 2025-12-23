<script setup>
defineProps({
  label: String,
  type: String,
  large: Boolean,
})
</script>

<template>
  <button v-if="type == 'primary'" class="primary-btn" :class="{ 'xl-btn': large }">
    {{ label }}
  </button>
  <button v-if="type == 'secondary'" class="secondary-btn">{{ label }}</button>
  <button v-if="type == 'ternary'" class="ternary-btn">
    {{ label }}
    <svg xmlns="http://www.w3.org/2000/svg" width="43" height="14">
      <g fill="none" fill-rule="evenodd" stroke="white">
        <path d="M0 7h41.864M35.428 1l6 6-6 6" />
      </g>
    </svg>
  </button>
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

.ternary-btn {
  color: var(--white-900);
  text-decoration-color: transparent;
  background: none;
  display: flex;
  align-items: center;
  gap: 1rem;
  width: fit-content;
  margin-left: auto;
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

@media (max-width: 800px) {
  button {
    font-size: 15px;
    letter-spacing: 2.5px;
  }
  .xl-btn {
    width: calc(100% - 2rem);
    height: 52px;
  }
}
</style>
