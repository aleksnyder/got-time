<script setup lang="ts">
  import TimeForm from './components/TimeForm.vue'
</script>

<template>
  <header>
    <div class="wrapper">
      <h1>got time?</h1>
      <p class="intro-text">Probably not.  That's why you're here isn't it?  Time is in short supply, let's create some out of thin air!</p>
    </div>
  </header>

  <main>
    <TimeForm />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

h1 {
  color: var(--color-heading);
  font-weight: 600;
  font-size: 5rem;
  position: relative;
  top: -10px;
  text-shadow: #222 1px 0 1px;
}

.intro-text {
  font-size: 1.5rem;
  font-weight: 500;
  line-height: 1.2;
  margin: 0 0 2rem;
  text-shadow: #222 1px 0 1px;
  color: rgba(255, 255, 255, 0.9);
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    justify-content: center;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
