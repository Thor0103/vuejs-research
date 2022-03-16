<template>
  <div>
    <form>
      <InputField label="Email:" type="email" />

      <InputField label="Password:" type="password" />

      <button type="submit">Login</button>
    </form>
  </div>
</template>

<script>
import InputField from "@/components/InputField";

export default {
  name: "LoginView",
  components: {
    InputField,
  },
};
</script>

<style scoped></style>
