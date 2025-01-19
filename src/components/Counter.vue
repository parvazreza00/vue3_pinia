<script setup>
import { ref,reactive, computed } from 'vue';
const count = ref(0);
const counterData = reactive({
    count: 0,
    title: 'Counter Title'
});
const oddOrEven = computed(()=>{
    return counterData.count % 2===0 ? "Even" : "Odd"
})
const increase = () => counterData.count++;
const decrease = () => counterData.count--;


</script>

<template>
   
    <div class="flex items-center justify-center space-x-4">
        <h3>Counter value is : {{ oddOrEven }}</h3>
        <button @click.prevent="increase()" class="bg-blue-500 hover:bg-blue-600 text-white p-2 rounded">Increment</button>
        <span>{{ counterData.count }}</span>
        <button @click.prevent="decrease()" :disabled="counterData.count === 0" :class="{'p-2 rounded bg-blue-500 hover:bg-blue-600 text-white': counterData.count > 0, 'p-2 rounded text-red-900 bg-gray-400 cursor-not-allowed text-gray-700': counterData.count === 0}">Decrement</button>
       
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