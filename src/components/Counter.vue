<template>
  <div>
    <div>Counter: {{ counter }}</div>
    <br />
  
    <button type="button" v-on:click="increase()">Click to increase</button>
    <button type="button" v-on:click="decrease()">Click to decrease</button>
    <button type="button" v-on:click="reset()">Click to reset</button>
  </div>
</template>

<script>
export default {
  name: "Counter",
  data: function () {
    return {
      counter: 0,
    };
  },
  methods: {
    increase: function () {
      this.counter++;
    },
    decrease: function () {
      this.counter--;
    },
    reset: function () {
      this.counter = 0;
    },
  },
};
</script>

<style>
#helloText {
  color: #178bff;
}
</style>