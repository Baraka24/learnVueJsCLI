<template>
<div>
    <a class="u-link-white" href="#" @click="toggleTimer">
    {{ time }}
    </a>
</div>
</template>

<script>
export default {
    data() {
    return {
      time: 0,
      isRunning: false,
      interval: null
    }
  },
  methods: {
    toggleTimer() {
      if (this.isRunning) {
        clearInterval(this.interval);
        console.log('timer stops');
      } else {
        this.interval = setInterval(this.incrementTime, 1000);
      }
      this.isRunning = !this.isRunning
    },
    incrementTime() {
      this.time = parseInt(this.time) + 1;
    },
  }
}
</script>
