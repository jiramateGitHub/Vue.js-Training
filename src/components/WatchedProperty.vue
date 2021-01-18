<template>
  <div id="example">
    <div id="demo">{{ fullName }}</div>
    <div id="demo2">{{ fullName2 }}</div>
    <button type="button" v-on:click="setName()">Click to changeName</button>
  </div>
</template>

<script>
export default {
  name: "WatchedProperty",
  data: function () {
    return {
      firstName: "Foo",
      lastName: "Bar",
      fullName: "Foo Bar",
    };
  },
  methods: {
    setName: function () {
      this.fullName2 = 'John Doe'
    },
  },
  watch: {
    firstName: function (val) {
      this.fullName = val + " " + this.lastName;
    },
    lastName: function (val) {
      this.fullName = this.firstName + " " + val;
    },
  },
  computed: {
    fullName2: {
      get: function () {
        return this.firstName + " // " + this.lastName;
      },
      set: function (newValue) {
        var names = newValue.split(" ");
        this.firstName = names[0];
        this.lastName = names[names.length - 1];
      },
    },
  },
};
</script>