<template>
  <div class="min-h-screen bg-grey-darker p-8">
    <div class="max-w-sm mx-auto">
      <UserSetting />
    </div>
  </div>
</template>

<script>
import UserSetting from "@/components/UserSetting";

export default {
  name: "App",
  components: {
    UserSetting,
  },
};
</script>

<style>
@import "./assets/styles/app.css";
</style>
