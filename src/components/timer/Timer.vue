<template>
  <div>
    <div>
      <h1 v-if="isWorkingTime">Work Time!</h1>
      <h1 v-else>Break Time!</h1>
      <h2> {{ minutes }}:{{ seconds }}</h2>
      <button v-on:click="startTimer">Start</button>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Timer',
  props: {
    workTime: Number,
    breakTime: Number
  },
  data: function () {
    return {
      isWorkingTime: true,
      seconds: 5,
      minutes: 2,
      interval: ''
    }
  },
  methods: {
    startTimer: function () {
      this.interval = setInterval(this.updateTime, 1000)
    },
    updateTime: function () {
      if (this.seconds <= 0 && this.minutes <= 0) {
        clearInterval(this.interval)
        this.isWorkingTime = !this.isWorkingTime
        this.toggleTimer()
        return
      }

      if (this.seconds <= 0) {
        this.seconds = 60
        this.minutes -= 1
        return
      }
      this.seconds -= 1
    },
    toggleTimer: function () {
      if (this.isWorkingTime) {
        this.seconds = 60
      } else {
        this.seconds = 30
      }
    }
  }
}
</script>
