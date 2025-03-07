<script setup>
import {ref} from 'vue'

const count = ref(0)
const increment = (name, event) =>{
    count.value++;
    console.log(name);
    console.log(event.target.tagName);
}

const linkClicked = () =>{
    console.log("linked clicked");
}

const parentClick = () =>{
    console.log("parent clicked");
}
</script>

<template>
    <div>Event Handlers</div>
    <button @click="increment('Parvaz', $event)" class="bg-indigo-500 hover:bg-indigo-600 px-2 py-1 text-white rounded ">Click me</button>
    <p>Count : {{ count }}</p>
    <div @click.capture="parentClick">
        <a href="http://www.google.com" @click.stop.prevent="linkClicked">Click Here</a>
    </div>
</template>

<style scoped>

</style>