<script setup>
import { ref } from "vue";

const isAwesome = ref(true);
</script>

<template>
    <div>
        <hr style="border:1px solid black;margin-top:8px">
        <h1>Conditional Rendergin</h1> 
        <div>
            <button @click="isAwesome = !isAwesome"
            class="bg-blue-500 hover:bg-blue-600 px-2 rounded"
            >Toggle</button>
        </div>     
        <h1 v-if="isAwesome">Vue is Awesome!</h1>
        <h1 v-if="!isAwesome">Oh! No. Vue is not Awesome!</h1>
        
    </div>
</template>

<style scoped>

</style>