<script setup>
import { computed, reactive, ref } from "vue";

const employees = reactive(['emp1','emp2']);
const isEmployeePresent = computed(()=>{
    return employees.length > 0 ? "Yes, There Have more than one employee" : "No Employee";
})

const firstName = ref("Parvaz");
const lastName = ref("Reza");
const fullName = computed({
    get(){
        return firstName.value+' '+lastName.value;
    },
    set(newValue){
        [firstName.value, lastName.value] = newValue.split(' ');
    }
})

fullName.value = "Yeasin Ahmed";



</script>

<template>
    <div>
        <h1>I am from computedComponent</h1>
        <div>Employee Present: {{ isEmployeePresent }}</div>
        <div>My FullName is : {{ fullName }}</div>
    </div>
</template>

<style scoped>

</style>