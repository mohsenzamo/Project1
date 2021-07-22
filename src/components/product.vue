<template>
  <div class="container">
    <p>title: {{ title }}</p>
    <img class="image" :src="image" />
    <slot name="input"></slot>
    <p>price: {{ price }}</p>
  </div>
</template>

<script>
export default {
  props: ["title", "image", "price"],
  data() {
    return {};
  },
  methods: {},
};

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
</script>

<style>
.container {
  box-shadow: 0px 0px 8px 3px #ccc;
  border-radius: 24px;
  width: 200px;
  overflow: hidden;
  margin: 16px;
  padding-bottom: 16px;
}
.image {
  width: 200px;
  height: 200px;
  object-fit: cover;
}
</style>