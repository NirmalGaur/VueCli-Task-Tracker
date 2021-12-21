<template>
  <button @click="onClick()" :style="{ background: color }" class="btn">
    <!-- Instead of writing  v-on:click="" we can write @click="". 
       Instead of writing v-bind:style="" we can write :style="". -->
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    text: String,
    color: String,
  },
  methods: {
    onClick() {
      this.$emit("btn-click");
    },
  },
};
</script>
