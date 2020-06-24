<template>
  <div>
    <div id="">
      <h1 v-if="work_time > 0">Work Time!</h1>
      <h1 v-else>Break Time!</h1>
      <h2> {{ timer.minutes }}:{{ timer.seconds }}</h2>
      <button v-on:click="startTimer">Start</button>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Timer',
  props: ['startTime'],
  data: function () {
    return {
      work_time: 1,
      break_time: 0,
      timer: {
        minutes: 25,
        seconds: 0
      }
    }
  },
  methods: {
    startTimer: function () {

    },
    calcTime: function () {

    }
  }
}
</script>
