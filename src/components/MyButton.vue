<template>
  <button class="button is-primary" @click="onClick">
    <slot></slot>
  </button>
</template>

<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";

@Component({})
export default class MyButton extends Vue {
  onClick() {
    this.$emit("click");
  }
}
</script>

<style scoped>
button {
  border: 1px solid #eee;
  border-radius: 3px;
  background-color: #ffffff;
  cursor: pointer;
  font-size: 15pt;
  padding: 3px 10px;
  margin: 10px;
}
</style>
