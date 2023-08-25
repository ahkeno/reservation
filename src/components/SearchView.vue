<script setup>
import {ref} from 'vue';
const searchText = ref("");
const rating = ref("hight")
</script>
<template>
    <input type="text" placeholder="Search ..." v-model.trim="searchText">
    <h3 v-if="searchText!==''">Search result of <span>{{ searchText }} </span> and Rating <span>{{ rating }}</span> ....</h3>
    <div>
        <h4>Advance Search by Rating</h4>
        <input type="radio" value="hight" v-model="rating"> hight
        <input type="radio" value="low" v-model="rating"> low


    </div>
</template>
<style scoped>
    h3 span{
        color: #6868ac;
        font-weight: bold;
    }
</style>