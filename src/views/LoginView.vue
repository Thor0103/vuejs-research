<template>
  <div class="login">
    <div class="hear-text">
      <p>LOGIN QUICK</p>
    </div>
    <form autocomplete="off">
      <div class="input-icon">
        <InputField
          label="Email:"
          type="email"
          placeholder="Email"
          @onChange="onChangeInput($event)"
        />
        <Icon class="icon" type="fas" key-name="faUserAstronaut" />
      </div>

      <div class="input-icon">
        <InputField placeholder="Password" label="Password:" type="password" />
        <Icon class="icon" type="fas" key-name="faKey" />
      </div>

      <div class="link">
        <router-link to="/forgot-password"> Forgot Password? </router-link>
      </div>

      <div class="btlogin">
        <button :disabled="isButtonDisabled" type="submit">Login</button>
      </div>
    </form>
  </div>
</template>

<script>
import InputField from "@/components/InputField";
import Icon from "@/components/Icon";
export default {
  name: "LoginView",
  components: {
    InputField,
    Icon,
  },
  data() {
    return {
      email: "",
      isButtonDisabled: "",
    };
  },
  methods: {
    onChangeInput(value) {
      this.email = value;
      console.log("Login form get data from input field: ", value);
      console.log("Kieu du lieu: ", typeof value);
      if (value === "") {
        this.isButtonDisabled = true;
      } else {
        this.isButtonDisabled = false;
      }
    },
  },
};
</script>

<style scoped lang="scss">
.hear-text {
  text-align: center;
  p {
    font-weight: bold;
    font-size: 30px;
    color: #ffffff;
  }
}
.login {
  background-image: url("../../src/assets/images/image-login.jpg");
}

.input-icon {
  display: flex;
  height: 34px;
  background: none;
  border-radius: 20px;
  border: 1px solid #dddddd;
  margin-bottom: 10px;
  padding: 0 15px;
  align-items: center;

  .input-field {
    width: 100%;
    margin-right: 15px;
  }
}

.link {
  text-align: right;

  a {
    color: #ffffff;
  }
}

.btlogin {
  display: block;
  justify-content: space-between;
  align-items: center;
  text-align: center;
  margin: 20px 0;

  button {
    width: 130px;
    height: 35px;
    background: #ea2958;
    border-radius: 20px;
    border: none;
    color: #ffffff;
    font-weight: bold;
  }
}

.icon {
  color: #ea2958;
}
</style>
