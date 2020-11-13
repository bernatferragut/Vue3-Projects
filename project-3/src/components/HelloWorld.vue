<template>
  <div>
    {{ state.msg }}
  </div>
</template>

<script>
import { reactive } from 'vue';
export default {
    setup() {
    const state = reactive({
      msg : 'Hello World',
    });

    return {
      state,
    };
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
