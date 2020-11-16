<template>
  <h2>My Course Goal</h2>
  <h3 v-if="courseGoal.showGoal">{{ courseGoal.title }}</h3>
  <button @click="toggleGoal">Toggle Goal</button>
  <!-- Task 3: Manage data in three ways -->
  <!-- => Ref Object -->
  <!-- Task 4: Also solve the assignment with the Options API -->
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const myGoal = ref({
      title: 'Become a Vue Master',
      showGoal: true
    });

    function showHideGoal() {
      myGoal.value.showGoal = !myGoal.value.showGoal;
      console.log(myGoal.value.showGoal);
    }

    return {
      courseGoal: myGoal.value,
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
