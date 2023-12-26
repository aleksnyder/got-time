<script setup lang="ts">
  defineProps(['message'])
</script>

<template>
  <p class="time-message">Congratulations!  You've been given {{message}}!  Spend it wisely!  Or don't and come back here for even more totally legitimate, not fake time! **</p>
  <small class="disclaimer">** In case the tone isn't clear enough, the message above is sarcastic.  Time can't be generated, and the time you're trying to recover is gone forever.</small>
</template>

<style scoped>
  .time-message {
    font-size: 1.5rem;
    font-weight: 500;
    line-height: 1.2;
    margin: 0 0 2rem;
    text-shadow: #222 1px 0 1px;
    color: #fff;
    margin: 3rem 0;
  }

  .disclaimer {
    font-size: 0.75rem;
  }
</style>
