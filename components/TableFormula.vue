<script setup>
const formulas = ref({
  1: {
    label: 'UNLIMITED STORY POSTING',
    plans: { basic: true, pro: true, business: true },
  },
  2: {
    label: 'UNLIMITED PHOTO UPLOAD',
    plans: { basic: true, pro: true, business: true },
  },
  3: {
    label: 'EMBEDDING CUSTOM CONTENT',
    plans: { basic: false, pro: true, business: true },
  },
  4: {
    label: 'CUSTOMIZE METADATA',
    plans: { basic: false, pro: true, business: true },
  },
  5: {
    label: 'ADVANCED METRICS',
    plans: { basic: false, pro: false, business: true },
  },
  6: {
    label: 'PHOTO DOWNLOADS',
    plans: { basic: false, pro: false, business: true },
  },
  7: {
    label: 'SEARCH ENGINE INDEXING',
    plans: { basic: false, pro: false, business: true },
  },
  8: {
    label: 'CUSTOM ANALYTICS',
    plans: { basic: false, pro: false, business: true },
  },
})
</script>

<template>
  <section>
    <TableRow v-for="formula in formulas" :key="formula.label" :formula="formula"/>
  </section>
</template>

<style scoped></style>
