<template>
  <div>

    <div>
      <h1 v-show="work_time == 0">Currently Working</h1>

    </div>
  </div>
</template>
<script>

function timer() {

}

export default {
  name: Timer,
  data: {
    work_time: 0,
    break_time: 0
  }

}
</script>
