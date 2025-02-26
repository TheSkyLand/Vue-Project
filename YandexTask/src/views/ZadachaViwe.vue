<script setup>
import LeapYear from '@/components/LeapYear.vue';
let year = 0;


let YearState = " "
const Play = () => {
if ((year % 400) == 0) 
{
    YearState = "Leap Year";
}
else if ((year % 100) === 0) {
    YearState = "Not a Leap Year";
} 
else if ((year % 4) == 0) {
    YearState = "Leap Year";
}
else {
    YearState = "Not a Leap Year";
}
}
</script>

<style>
</style>

<template>
<input type="number" min="0" v-model="year" onkeydown="return event.key !== '-';">
<h1>Welcome to {{ year }} year!</h1>

<button @click="Play()">Calculate</button>
    <h1>the year is: {{ YearState }}</h1>
</template>