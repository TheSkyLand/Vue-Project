<script setup>
var KStr = [4, 12]
var NStr = [5, 10, 15, 20, 3, 6, 9, 25, 30, 12, 21, 24];

var SashaScore = 0;
var LenaScore = 0;
var WinnerString = ' ';

const play = () => {
    for (var i = 0; i < NStr.length; i++) {
        debugger
        if (((NStr[i] % 5) == 0) && ((NStr[i] % 3) == 0) || ((NStr[i] % 5) !== 0) && ((NStr[i] % 3) !== 0)) {

            continue;
        }
        else if (((NStr[i] % 5) == 0)) {
            LenaScore += 1;
        }
        else if (((NStr[i] % 3) == 0)) {
            SashaScore += 1;
        }


    }
    if (SashaScore > LenaScore) {
        WinnerString = 'sasha'
    }
    else if (SashaScore < LenaScore) {
        WinnerString = 'lena'
    }
    else {
        WinnerString = 'draw'

    }
    console.log(WinnerString)
    console.log(LenaScore, SashaScore);
}
</script>

<style></style>

<template>
    <button @click="play">
        active
    </button>
    <div>
    </div>
</template>
