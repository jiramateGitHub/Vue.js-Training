<template>
  <div v-bind:style="{ color: activeColor, fontSize: fontSize + 'px' }"></div>
</template>

<script>
export default {
  name: "BindingHtmlClasses",
  data: function () {
    return {
      isActive: true,
      error: null,
    };
  },
  computed: {
    classObject: function () {
      return {
        active: this.isActive && !this.error,
        "text-danger": this.error && this.error.type === "fatal",
      };
    },
  },
};
</script>