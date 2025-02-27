<script setup>
import { ref } from 'vue';

let year = ref(0);
let YearState = ref("");
const Play = () => {
    if (((year.value % 4) == 0) || ((year.value % 100) !== 0) && (year.value % 400) == 0) {
        YearState.value = "Leap Year";
    } else{
        YearState.value = "Not a Leap Year";
    }

}
</script>

<style></style>

<template>
    <input v-model="year" type="number" min="0" onkeydown="return event.key !== '-';">
    <h1>Welcome to {{ year }} year!</h1>

    <button @click="Play">Calculate</button>
    <h1>This is a {{ YearState }}.</h1>
</template>