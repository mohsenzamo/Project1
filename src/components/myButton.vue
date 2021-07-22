<template>
  <button @click="deleteButton"><slot name="button"></slot></button>
</template>

<script>
export default {
  data() {},
  methods: {
    deleteButton() {
      this.$emit("delete-clicked");
    },
  },
};
</script>

<style scoped>
button {
  width: 140px;
  background-color: tomato;
  color: white;
  box-shadow: 0px 0px 8px 2px #ccc;
  outline: none;
  cursor: pointer;
  border: none;
  padding: 8px;
  border-radius: 8px;
}
</style>