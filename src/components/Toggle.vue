<template>
  <span
    class="toggle flex-no-shrink"
    role="checkbox"
    tabindex="0"
    @click="toggleNewsletter"
    @keydown.space.prevent="toggleNewsletter"
    :aria-checked="receiveNewsletter.toString()"
  ></span>
</template>

<script>
export default {
  props: {
    receiveNewsletter: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    toggleNewsletter() {
      this.$emit("update:receiveNewsletter", !this.receiveNewsletter);
    },
  },
};
</script>
