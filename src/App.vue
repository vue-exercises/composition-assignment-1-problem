<template>
  <h2>My Course Goal</h2>
  <h3 v-if="showGoal">{{ courseGoal }}</h3>
  <button @click="showHideGoal">Toggle Goal</button>
</template>

<script>
export default {
  data() {
    return {
      courseGoal: 'Become a Vue Master',
      showGoal: true
    };
  },
  methods: {
    showHideGoal() {
      this.showGoal = !this.showGoal;
    }
  }
};
</script>

<style>
html {
  font-family: sans-serif;
}
body {
  margin: 3rem;
  text-align: center;
}
</style>
