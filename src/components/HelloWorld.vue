<template>
  <div class="hello">
    <p>
      Enter owner name and the thing that is owned:
      <input
        v-model="ownerName"
        placeholder="enter owner"
      >
      <input v-model="thing" placeholder="enter thing">
    </p>
    <span>{{ ownerName }}</span>
    <span>has a</span>
    <span>{{ thing }}</span>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      ownerName: "e.g Old McDonald",
      thing: "e.g cow"
    };
  },
  computed: {
    // a computed getter
    ownerHasThing: function() {
      // `this` points to the Vue instance's data option
      return this.ownerName + " " + this.thing;
    }
  }
};
</script>

