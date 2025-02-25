<script setup>




</script>

<style></style>

<template>
    <div>
        <input v-mod type="number" min="1" max="1000" v-model="KString" placeholder="Enter K" />

        <span>K:{{ KString }}</span>
    </div>
    <div>
        
        <input type="number" min="1" max="1000" v-model="NString" placeholder="Enter N" />

        <span>N:{{ NString }}</span>
    </div>
    <button @click="console.log( KString ,  NString)">
        active
    </button>
    <div>
        winner: {{ WinnerString }}
    </div>
</template>