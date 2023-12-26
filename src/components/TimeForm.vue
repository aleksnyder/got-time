<script setup lang="ts">
import { ref } from 'vue'
  import TimeMessage from "./TimeMessage.vue";

  let showMessage = ref(false);
  let randomTimeMessage = ref('0:0:00 AM')

  const randomTime = () => {
    const randomHours = Math.floor(Math.random() * 24);
    const randomHoursFormat = randomHours === 1 ? `${randomHours} hour` : randomHours > 0 ? `${randomHours} hours`: ''
    return String(randomHoursFormat);
  }

  const generateMessage = () => {
    showMessage.value = true;
    randomTimeMessage.value = randomTime();
  };
</script>

<template>
  <div class="btn-wrapper">
    <button class="randomizer" type="button" @click="generateMessage">Generate time</button>
  </div>
  <TimeMessage v-if="showMessage" :message="randomTimeMessage" />
</template>

<style scoped>
  .time-form {
    display: flex;
    flex-flow: row nowrap;
    gap: 2rem;
    margin: 0 0 3rem;
  }

  .time-input {
    display: flex;
    flex-flow: column nowrap;
    gap: 0.5rem;
  }

  .time-input__label {
    font-weight: 600;
    color: var(--color-heading);
  }

  .btn-wrapper {
  display: flex;
  gap: 1rem;
}

.randomizer {
  background-color: hsla(160, 100%, 37%, 0.75);
}

.randomizer:hover {
  background-color: hsla(160, 100%, 37%, 0.5);
}
</style>
