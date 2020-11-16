<template>
  <h2>My Course Goal</h2>
  <h3 v-if="boolGoal">{{ courseGoalTitle }}</h3>
  <button @click="toggleGoal">Toggle Goal</button>
  <!-- Task 3: Manage data in three ways -->
  <!-- => Separate refs -->
  <!-- => Ref Object -->
  <!-- Task 4: Also solve the assignment with the Options API -->
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const myGoalTitle = ref('Become a Vue Master');
    let showGoal = ref(true);

    function showHideGoal() {
      showGoal.value = !showGoal.value;
    }

    return {
      courseGoalTitle: myGoalTitle,
      boolGoal: showGoal,
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
