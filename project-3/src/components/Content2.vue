<template>
    <div>
        CONTENT2
        <pre class="fng">{{ res2.data[0].value }}</pre>
    </div>
</template>

<script>

import {ref} from 'vue';

export default {
    name:'Content2',
    async setup(){

        let res2 = ref(null);
        let res1 = await fetch('https://api.alternative.me/fng/?limit=1&format=json&date_format=world');
        res2 = await res1.json();
        console.log(res2);

        return { res2 }
    }

}
</script>


<style>

.fng {
    font-size: 4em;
}

</style>