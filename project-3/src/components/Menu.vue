<template>
  <div>
    {{ state.msg.toUpperCase() }}
  </div>
</template>

<script>
import { reactive } from 'vue';
export default {
    setup() {
    const state = reactive({
      msg : 'MENU',
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
