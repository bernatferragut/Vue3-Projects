<template>
    <div>
        CONTENT2
        <p>{{ test }}</p>
    </div>
</template>

<script>

import {ref} from 'vue'

export default {
    setup(){

        let test = ref('Fear&Greed');

        return { test }
    }

}
</script>


<style>

</style>