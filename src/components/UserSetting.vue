<template>
  <form class="card" @submit.prevent="submit">
    <h1 class="text-2xl font-bold mb-6">Your Settings</h1>
    <label class="block mb-6">
      <span class="form-label mb-2">Email Address</span>
      <input v-model="email" class="form-input" placeholder="you@example.com" />
    </label>
    <div class="mb-8">
      <span class="form-label mb-2">Newsletter</span>
      <div class="flex justify-between items-center">
        <p class="mr-4">Send you occasional news and updates.</p>
        <Toggle v-model:receiveNewsletter="receiveNewsletter" />
      </div>
    </div>
    <div class="text-right">
      <button type="submit" class="btn btn-blue">Update Settings</button>
    </div>
  </form>
</template>

<script>
import Toggle from "./Toggle";
export default {
  components: {
    Toggle,
  },
  props: [],
  data() {
    return {
      email: "jane@example.com",
      receiveNewsletter: false,
    };
  },
  methods: {
    submit() {
      console.log("Submitting preferences...", {
        email: this.email,
        receiveNewsletter: this.receiveNewsletter,
      });
    },
  },
};
</script>
<style scoped>
@import "../assets/styles/app.css";
</style>>
