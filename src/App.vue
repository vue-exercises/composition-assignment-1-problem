<template>
  <h2>My Course Goal</h2>
  <h3 v-if="courseGoal.showGoal">{{ courseGoal.title }}</h3>
  <button @click="toggleGoal">Toggle Goal</button>
  <!-- Task 3: Manage data in three ways -->
  <!-- => Separate refs -->
  <!-- => Ref Object -->
  <!-- => Reactive Object -->
  <!-- Task 4: Also solve the assignment with the Options API -->
</template>

<script>
import { reactive } from 'vue';

export default {
  setup() {
    const myGoal = reactive({
      title: 'Become a Vue Master',
      showGoal: true
    });

    function showHideGoal() {
      myGoal.showGoal = !myGoal.showGoal;
    }

    return {
      courseGoal: myGoal,
      toggleGoal: showHideGoal
    };
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
