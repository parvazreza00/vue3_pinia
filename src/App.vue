<script setup>
import Counter from "./components/Counter.vue";
import TemplateSyntax from "./components/TemplateSyntax.vue";
import ComputedComponent from "./components/ComputedComponent.vue";
import StyleBinding from "./components/StyleBinding.vue";
import ConditionalRendering from "./components/ConditionalRendering.vue";
</script>

<template>
  <section class="container mx-auto">
    <div>
      <h1>App Component</h1>
    </div>
    <div>      
      <ComputedComponent/>
    </div>
    <div>
      <Counter/>
    </div>
    <div>
      <StyleBinding/>
    </div>    
      <ConditionalRendering/>
    
  </section>
</template>

<style scoped></style>
