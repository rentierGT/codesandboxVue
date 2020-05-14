<template>
  <button v-on:click="handleClick">Click</button>
</template>

<script>
export default {
  name: "Child",
  methods: {
    handleClick: function() {
      this.$emit("child-notification", "Info from child");
    }
  }
};
</script>
