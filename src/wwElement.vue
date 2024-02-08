<template>
  <div class="my-element">
    <p :style="textStyle">I am a custom element, my friend person!</p>
    <p>My message is: {{ message }}</p>
  </div>
</template>

<script>
export default {
  props: {
    content: { type: Object, required: true },

  },
  computed: {
    textStyle() {
      return {
        color: this.content.textColor,
      };
    },
    message: function () {
      return this.content.message;
    },

  },
};
</script>

<style lang="scss" scoped>
.my-element {
  p {
    font-size: 18px;
  }
}
</style>
