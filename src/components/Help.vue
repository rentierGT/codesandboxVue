<template>
  <div>
    <Child v-on:child-notification="handleNotification"/>
    <p>Event-Result: {{ childMessage }}</p>
  </div>
</template>

<script>
import Child from "./Child";

export default {
  name: "Help",
  data: function() {
    return {
      childMessage: ""
    };
  },
  components: {
    Child
  },
  methods: {
    handleNotification: function(msg) {
      this.childMessage = msg;
    }
  }
};
</script>