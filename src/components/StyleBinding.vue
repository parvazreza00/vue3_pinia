<script setup>
import { reactive, ref, computed } from "vue";

const activeColor = ref("red");
const fontSize = ref(30);

const style1 = reactive({
    color: 'dodgerblue',
    fontSize:'35px'
});

const style2 = reactive({
    color:'gray',
    border:'2px solid green',
})

const styleObj = computed(() => {
  return {
    color: activeColor.value,
    fontSize: fontSize + "px",
  };
});

setTimeout(() => {
  console.log("Fired");
  activeColor.value = "blue";
}, 5000);

</script>

<template>
  <div>
    <hr style="border: 1px solid black" class="mt-3" />
    <h1 :style="[style1, style2]">Style Binding</h1>
  </div>
</template>

<style scoped></style>
