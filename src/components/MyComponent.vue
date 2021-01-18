<template>
  <div id="helloText">
    <div>Hello by {{ msg }}</div>
    <br>
  </div>
</template>

<script>
export default {
  name: "MyComponent",
  props: ["msg"],
};
</script>

<style>
#helloText {
  color: #178bff;
}
</style>