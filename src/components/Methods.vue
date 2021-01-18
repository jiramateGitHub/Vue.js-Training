<template>
  <div id="example">
    <p>Date: "{{ now }}"</p>
    <p>Date from Method: "{{ reverseMessageInMethod() }}"</p>
    <p>Date from Computed: "{{ reversedMessageInComputed }}"</p> <br />
    <button type="button" v-on:click="changeDate()">Click to update date</button>
  </div>
</template>

<script>
export default {
  name: 'MyComponent',
  data: function () {
    return {
      now: Date.now()
    }
  },
  methods: {
    changeDate: function () {
      this.now = Date.now()
    },
    reverseMessageInMethod: function () {
      return Date.now()
    }
  },
  computed: {
    // a computed getter
    reversedMessageInComputed: function () {
      // `this` points to the vm instance
      return Date.now()
    }
  }
}
</script>