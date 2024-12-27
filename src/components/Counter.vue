<script setup>
import { ref,reactive } from 'vue';
const count = ref(0);
const counterData = reactive({
    count: 0,
    title: 'Counter Title'
});
const increase = () => counterData.count++;
const decrease = () => counterData.count--;

</script>

<template>
   
    <div class="flex items-center justify-center space-x-4">
        <h3>{{ counterData.title }}</h3>
        <button @click.prevent="increase()" class="bg-blue-500 hover:bg-blue-600 text-white p-2 rounded">Increment</button>
        <span>{{ counterData.count }}</span>
        <button @click.prevent="decrease()" class="bg-blue-500 hover:bg-blue-600 text-white p-2 rounded">Decrement</button>
        <input type="text" v-model="counterData.title" class="p-2 border border-gray-300 rounded">
    </div>
</template>


// <script>
// export default {
//    data(){
//     return {
//         count: 0
//     };
//    },
//    methods: {
//        increase(){
//            this.count++;
//        },
//        decrease(){
//            this.count--;
//        }
//    }
// }
// </script>

<style scoped>

</style>