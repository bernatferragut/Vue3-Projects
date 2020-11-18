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
      msg : 'SEARCH',
    });

    return {
      state,
    };
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

</style>
