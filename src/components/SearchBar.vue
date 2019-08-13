<template>
  <div>
    <input class="input-group-text" @input="onInput" placeholder="Search for video"/>
  </div>
</template>

<script>
export default {
  name: "SearchBar",
  methods: {
    onInput: function(event) {
      this.$emit("termChange", event.target.value);
    }
  }
};
</script>

<style scoped>
input {
  width: 80%;
  margin: 0 auto;
}
div {
  text-align: center;
  margin: 20px 5px;
}
</style>

