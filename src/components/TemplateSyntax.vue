<template>
  <div class="TemplateSyntax">
    <span>Message: {{ msg }}</span>
    <span v-once>This will never change: {{ msg }}</span>
    <p>Using mustaches: {{ rawHtml }}</p>
    <p>Using v-html directive: <span v-html="rawHtml"></span></p>
    <div v-bind:id="dynamicId"></div>
    <button v-bind:disabled="isButtonDisabled">Button</button>
    {{ number + 1 }}

    {{ ok ? "YES" : "NO" }}

    {{ message.split("").reverse().join("") }}

    <div v-bind:id="'list-' + id"></div>

    <!-- full syntax -->
    <a v-bind:href="url"> ... </a>

    <!-- shorthand -->
    <a :href="url"> ... </a>

    <!-- full syntax -->
    <a v-on:click="doSomething"> ... </a>

    <!-- shorthand -->
    <a @click="doSomething"> ... </a>
  </div>
</template>

<script>
export default {
  name: "TemplateSyntax",
  props: {
    msg: String,
  },
};
</script>