<template v-if="ok">
  <div>
    <h1 v-if="true">Yes</h1>

    <h1 v-if="Math.random() > 0.5">Yes</h1>

    <div v-if="type === 'A'">A</div>
    <div v-else-if="type === 'B'">B</div>
    <div v-else-if="type === 'C'">C</div>
    <div v-else>Not A/B/C</div>
    
    <h1 v-show="true">Hello!</h1>
  </div>
</template>

<script>
export default {
  name: "ConditionalRendering",
};
</script>