<template>
  <h1>Counts: {{ state.count }}, Double: {{ state.double }}</h1>
  <div>
      <button @click="updateCount(true)">+</button>
      <button @click="updateCount(false)">-</button>
  </div>
</template>

<script>

// import { ref } from 'vue';
import { reactive , computed} from 'vue';

export default {

  setup() {
    let state = reactive({
      count : 0,
      double : computed(()=> state.count * 2),
    });

    function updateCount(increase) {
      if(increase){
        state.count++;
      } else {
        state.count--;
      }
    }

    return {
      state,
      updateCount,
    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
