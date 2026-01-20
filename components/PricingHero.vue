<script setup></script>

<template>
  <section class="mx-width">
    <h2 class="tp-1">We’re in beta.<br />Get your invite <br />today!</h2>
    <Button type="ternary" label="get an invite" large="false" />
  </section>
</template>

<style scoped>
section {
  background-color: limegreen;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-block: 3rem;
  background-image: url('/images/shared/desktop/bg-beta.jpg');
  background-repeat: no-repeat;
  background-size: cover;
}

h2 {
  color: var(--white-900);
}

@media (max-width: 1024px) {
  section {
    background-image: url('/images/shared/tablet/bg-beta.jpg');
  }
}

@media (max-width: 850px) {
  section {
    background-image: url('/images/shared/mobile/bg-beta.jpg');
  }
}
</style>
