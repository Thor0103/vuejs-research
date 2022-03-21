<template>
  <div class="input-field">
    <label>
      <input
        :placeholder="placeholder"
        :type="type"
        v-model="inputValue"
        autocomplete="off"
      />
    </label>
  </div>
</template>

<script>
export default {
  name: "InputField",
  props: {
    label: {
      type: String,
      default: "Field",
    },
    type: {
      type: String,
      default: "number",
    },
    placeholder: {
      type: String,
      default: "Input placehoder",
    },
    onChange: {
      type: Function,
    },
  },
  data() {
    return {
      inputValue: "",
    };
  },
  created() {},
  mounted() {},
  watch: {
    inputValue: {
      handler(value) {
        console.log("inputValue changed: ", value);
        this.$emit("onChange", value);
      },
    },
  },
};
</script>

<style scoped lang="scss">
$coler-label: red;
$font-label: Helvetica, sans-serif;
$fontsize: 1rem;

.input-field {
  display: flex;
  align-items: center;

  label {
    width: 100%;
    height: 100%;
  }

  input {
    width: 100%;
    height: 100%;
    border: none;
    outline: none;
    background: none;

    &:-ms-input-placeholder {
      /* Internet Explorer 10-11 */
      color: red;
    }

    &::-webkit-input-placeholder {
      /* Edge */
      color: red;
    }

    &::placeholder {
      color: #ffffff;
    }
  }
}
</style>
