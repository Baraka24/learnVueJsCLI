<template>
<div>
    <div id="clock">
        <div id="hours">{{ Math.floor((time/60)/60) }} HEURE</div>
        <div>:</div>
        <div id="minutes">{{ Math.floor(time/60) }} MINUTE</div>
        <div>:</div>
        <div id="seconds">{{ time }} SECO</div><br>
    </div>
    <a class="play-btn" href="#" @click="toggleTimer"></a>
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

<style>
body {
  background: #faf7f7;
}

.play-btn {
  width: 100px;
  height: 100px;
  background: radial-gradient( rgba(18, 118, 168) 60%, rgba(255, 255, 255, 1) 62%);
  border-radius: 50%;
  position: relative;
  display: block;
  margin: 100px auto;
  box-shadow: 0px 0px 25px 3px rgba(37, 164, 218);
}

/* triangle */
.play-btn::after {
  content: "";
  position: absolute;
  left: 50%;
  top: 50%;
  -webkit-transform: translateX(-40%) translateY(-50%);
  transform: translateX(-40%) translateY(-50%);
  transform-origin: center center;
  width: 0;
  height: 0;
  border-top: 15px solid transparent;
  border-bottom: 15px solid transparent;
  border-left: 25px solid #fff;
  z-index: 100;
  -webkit-transition: all 400ms cubic-bezier(0.55, 0.055, 0.675, 0.19);
  transition: all 400ms cubic-bezier(0.55, 0.055, 0.675, 0.19);
}

/* pulse wave */
.play-btn:before {
  content: "";
  position: absolute;
  width: 150%;
  height: 150%;
  -webkit-animation-delay: 0s;
  animation-delay: 0s;
  -webkit-animation: pulsate1 2s;
  animation: pulsate1 2s;
  -webkit-animation-direction: forwards;
  animation-direction: forwards;
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
  -webkit-animation-timing-function: steps;
  animation-timing-function: steps;
  opacity: 1;
  border-radius: 50%;
  border: 5px solid rgba(255, 255, 255, .75);
  top: -30%;
  left: -30%;
  background: rgba(198, 16, 0, 0);
}

@-webkit-keyframes pulsate1 {
  0% {
    -webkit-transform: scale(0.6);
    transform: scale(0.6);
    opacity: 1;
    box-shadow: inset 0px 0px 25px 3px rgba(255, 255, 255, 0.75), 0px 0px 25px 10px rgba(255, 255, 255, 0.75);
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
    opacity: 0;
    box-shadow: none;

  }
}

@keyframes pulsate1 {
  0% {
    -webkit-transform: scale(0.6);
    transform: scale(0.6);
    opacity: 1;
    box-shadow: inset 0px 0px 25px 3px rgba(255, 255, 255, 0.75), 0px 0px 25px 10px rgba(255, 255, 255, 0.75);
  }
  100% {
    -webkit-transform: scale(1, 1);
    transform: scale(1);
    opacity: 0;
    box-shadow: none;

  }
}
#clock {
            display: flex;
            justify-content: center;
            align-items: center;
            /* height: 100vh; */
        }
        #clock > div {
            /* margin: 0 10px; */
            font-size: 3rem;
        }
</style>
