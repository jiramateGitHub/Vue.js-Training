<template v-if="ok">
  <div>
    <li v-for="item in items" v-bind:key="item">
      {{ item.message }}
    </li>

    <li v-for="(item, index) in items" v-bind:key="item">
      {{ parentMessage }} - {{ index }} - {{ item.message }}
    </li>

    <ul id="v-for-object" class="demo">
      <li v-for="value in object" v-bind:key="value">
        {{ value }}
      </li>
    </ul>

    <div v-for="(value, key) in object" v-bind:key="value">
      {{ key }}: {{ value }}
    </div>

    <div v-for="(value, key, index) in object" v-bind:key="value">
      {{ index }}. {{ key }}: {{ value }}
    </div>

    <div v-for="item in items" :key="item.id">
      <!-- content -->
      <h1>Test</h1>
    </div>

    <li v-for="n in evenNumbers" v-bind:key="n">{{ n }}</li>
  </div>
</template>

<script>
export default {
  name: "ListRendering",
  data: function () {
    return {
      parentMessage: "Parent",
      items: [{ message: "Foo" }, { message: "Bar" }],
      object: {
        firstName: "John",
        lastName: "Doe",
        age: 30,
      },
      numbers: [1, 2, 3, 4, 5],
    };
  },
  computed: {
    evenNumbers: function () {
      return this.numbers.filter(function (number) {
        return number % 2 === 0;
      });
    },
  },
};
</script>