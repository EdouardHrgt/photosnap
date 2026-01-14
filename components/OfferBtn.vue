<script setup>
const yearly = ref(false)

const togglePlan = () => {
  yearly.value = !yearly.value
}
</script>

<template>
  <div class="monthly-yearly">
    <p>
      <strong class="tp-3">Monthly</strong>
    </p>
    <span class="toggler" @click="togglePlan">
      <span class="ball" :class="{ active: yearly }"></span>
    </span>
    <p>
      <strong class="tp-3">Yearly</strong>
    </p>
  </div>
</template>

<style scoped>
.monthly-yearly {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 2rem;
  margin-block: 5rem;
}

.toggler {
  background-color: rgb(218, 218, 218);
  width: 64px;
  height: 32px;
  border-radius: 18px;
  display: flex;
  align-items: center;
  position: relative;
  cursor: pointer;
}

.ball {
  display: block;
  background-color: rgb(75, 75, 75);
  border-radius: 100%;
  width: 24px;
  aspect-ratio: 1 / 1;
  position: absolute;
  left: 5px;
  transition: all 0.3s;
}

.ball.active {
  left: 35px;
}
</style>
