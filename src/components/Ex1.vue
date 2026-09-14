<script setup>

import { ref } from 'vue';

const id = ref('circle')


function mOver() {
    // add code here
    // the shape changes to square on mouse over
    id.value = 'square'

}

function mOut() {
    // add code here
   // the shape changes back to circle on mouse out event
    id.value = 'circle'
}
</script>

<template>
    <!-- modify code below -->
    <div v-bind:id="id" @mouseover="mOver" @mouseout="mOut">
        Mouse Over Me
    </div>

</template>

<style scoped>
#square {
    width: 150px;
    height: 150px;
    background-color: goldenrod;
    text-align: center;
    padding-top: 60px;
}

#circle {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    background-color: goldenrod;
    text-align: center;
    padding-top: 60px;
}
</style>