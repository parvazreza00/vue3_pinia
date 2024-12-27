<script setup>
const message = '<h1>Hello World!</h1>';
const dynamcId ="my_id";
const objectAttr = {
    id: 'my_id',
    class: 'text-5xl bg-blue-500 text-white p-2 rounded'
}

const title = "title";
const titleValue = "THis is title"
const eventName = 'click';
const clickme = () => {
    alert('Clicked');
}
</script>

<template>
    <div v-html="message" ></div>
    <div  :id="dynamcId">Dynamic ID</div>
    <div v-bind="objectAttr" :[title]="titleValue">Object attribute binding</div>
    <div class="">{{Math.random()}}</div>
    <div class="" @[eventName]="clickme()"><button>Click me</button></div>





</template>

<style scoped>

</style>