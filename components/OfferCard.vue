<script setup>
const props = defineProps({
  card: Object,
  period: String,
})

const priceIndex = computed(() => props.period === 'month' ? 0 : 1)
</script>

<template>
  <article :class="{ main: card.main }">
    <h3 class="tp-2">{{ card.label }}</h3>
    <p class="tp-body description">
      {{ card.text }}
    </p>
    
    <Transition name="fade" mode="out-in">
      <p :key="priceIndex">
        <strong class="tp-1">${{ card.prices[priceIndex].toFixed(2) }}</strong>
      </p>
    </Transition>
    
    <Transition name="fade" mode="out-in">
      <p class="tp-body" :key="priceIndex">
        per {{ card.durations[priceIndex] }}
      </p>
    </Transition>

    <button class="tp-4">PICK PLAN</button>
  </article>
</template>

<style scoped>
article {
  padding-inline: 2.5rem;
  padding-block: 3rem;
  background-color: var(--grey-400);
  border-radius: 5px;
}

h3 {
  margin-bottom: 1rem;
}

.description {
  margin-bottom: 2rem;
  min-height: 6rem;
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

article.main {
  background-color: var(--black-900);
  min-height: 500px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-top: -43px;
  position: relative;
}

article.main::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 5px;
  background: linear-gradient(to right, var(--blue-400), var(--purple-400), var(--yellow-400));
  border-radius: 5px 5px 0 0;
}

article.main h3,
article.main p,
article.main strong {
  color: var(--white-900);
}

article.main button {
  background-color: var(--white-900);
  color: var(--black-900);
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}


@media (max-width: 1024px) {
article.main {
  min-height: unset;
  display: block;
  margin-top: 0;
}
article.main::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: auto;
  height: 100%;
  width: 5px;
  background: linear-gradient(to bottom, var(--blue-400), var(--purple-400), var(--yellow-400));
  border-radius: 0;
}
article {
  width: 100%;
  border-radius: 0;
}
.description {
  min-height: unset;
}
}
</style>