<template>
  <div class="input-field">
    <label>
      <span class="label">{{ label }}</span>
      <input :type="type" />
    </label>
  </div>
</template>

<script>
export default {
  name: "InputField",
  props: {
    label: String,
    type: String,
  },
};
</script>

<style scoped lang="scss">
.label {
  color: red;
  font-size: 1rem;
}
</style>
