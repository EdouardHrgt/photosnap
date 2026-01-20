<script setup>
defineProps({
  formula: Object,
})
</script>

<template>
  <section>
    <h4 class="">{{ formula.label }}</h4>
    <div class="formulas-container">
      <div class="formula">
        <p class="">basic</p>
        <svg v-if="formula.plans.basic" xmlns="http://www.w3.org/2000/svg" width="18" height="15">
          <path fill="none" stroke="#000" stroke-width="2" d="M1 8.124L5.623 13 17 1" />
        </svg>
      </div>
      <div class="formula">
        <p class="">pro</p>
        <svg v-if="formula.plans.pro" xmlns="http://www.w3.org/2000/svg" width="18" height="15">
          <path fill="none" stroke="#000" stroke-width="2" d="M1 8.124L5.623 13 17 1" />
        </svg>
      </div>
      <div class="formula">
        <p class="">business</p>
        <svg v-if="formula.plans.business" xmlns="http://www.w3.org/2000/svg" width="18" height="15">
          <path fill="none" stroke="#000" stroke-width="2" d="M1 8.124L5.623 13 17 1" />
        </svg>
      </div>
    </div>
  </section>
</template>

<style scoped>
h4 {
    margin-top: 2rem;
}

.formulas-container {
  display: flex;
  gap: 4rem;
  margin-top: 0.6rem;
  border-bottom: 3px solid var(--grey-400);
  padding-bottom: 1.5rem;
}

.formula {
  text-transform: uppercase;
  text-align: center;
  color: var(--grey-dark);
  font-size: var(--fs-500);
  line-height: 25px;
  letter-spacing: 1px;
  font-weight: var(--fw-400);
}

.formula svg {
  display: block;
  margin-inline: auto;
  margin-top: 0.1rem;
}
</style>
