<script setup>
const K = 3
const N = 1

let SashaScore;
let LenaScore;
const play = () => {
    if ((N % 5) == 0){
        LenaScore++;
    }
    if ((N % 3) == 0) {
        SashaScore++;
    }
    if (((N % 3) == 0) && ((N % 5) == 0) && ((N % 3) !== 0) && ((N % 5) !== 0)) 
    {
        LenaScore += 0;
        SashaScore += 0;  
    }
    if (SashaScore > LenaScore) {
        WinnerString = 'sasha'
    }
    else if (LenaScore > SashaScore) {
        WinnerString = 'lena'
    }
    else {
        WinnerString = 'draw'
    }
}
</script>

<style></style>

<template>
    <button @click="play" >
        active
    </button>
    <div>
        winner: {{ WinnerString }}
    </div>
</template>
