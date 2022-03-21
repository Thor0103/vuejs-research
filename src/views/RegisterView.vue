<template>
  <div class="login">
    <div class="header-reg">
      <div class="icon">
        <Icon class="icon" type="fas" key-name="faCircleArrowLeft" />
      </div>
      <div class="header-reg-text">Sign Up</div>
    </div>

    <div class="header-text">
      <p>Register Qick</p>
    </div>

    <div class="header-camera">
      <div class="camera">
        <Icon class="icon" type="fas" key-name="faCameraRetro" />
      </div>
    </div>
    <div class="main-input">
      <div class="children-input">
        <Icon class="icon" type="fas" key-name="faUserAstronaut" />
        <InputField
          class="input-reg"
          placeholder="First name"
          label="First Name"
          type="text"
        />
      </div>
      <div class="children-input">
        <Icon class="icon" type="fas" key-name="faPhone" />
        <InputField
          class="input-reg"
          placeholder="Phone"
          label="Phone"
          type="tel"
        />
      </div>
      <div class="children-input">
        <Icon class="icon" type="fas" key-name="faEnvelope" />
        <InputField
          class="input-reg"
          placeholder="Email"
          label="Email"
          type="email"
        />
      </div>
      <div class="children-input">
        <Icon class="icon" type="fas" key-name="faKey" />
        <InputField
          class="input-reg"
          placeholder="Password"
          label="Password"
          type="email"
        />
      </div>
    </div>

    <div class="regis-socical">
      <div class="socisal-gg">
        <button type="submit">
          <Icon class="icon" type="fab" key-name="faFacebookF" />
          <p>Facebook</p>
        </button>
      </div>

      <div class="socical-text">
        <p>or</p>
      </div>

      <div class="socisal-fb">
        <button type="submit">
          <div>
            <Icon class="icon" type="fab" key-name="faGoogle" />
          </div>
          <p>Google</p>
        </button>
      </div>
    </div>
  </div>
</template>
<script>
import InputField from "@/components/InputField";
import Icon from "@/components/Icon";
export default {
  name: "RegisterView",
  components: {
    InputField,
    Icon,
  },
  data() {},
};
</script>

<style scoped lang="scss">
.login {
  background-image: url("../../src/assets/images/image-login.jpg");
}

.header-text {
  font-weight: bold;
  font-size: 30px;
  color: #ffffff;
  text-align: center;
}

.header-reg {
  width: 100%;
  display: flex;

  .icon {
    text-align: left;
    color: #ffffff;
    font-size: 18px;
  }

  .header-reg-text {
    width: 100%;
    text-align: right;
    font-weight: 500;
    font-size: 18px;
    color: #fff;
  }
}

.header-camera {
  width: 100%;
  display: flex;
  margin-bottom: 20px;

  .camera {
    width: 100px;
    height: 100px;
    border-radius: 100%;
    border: 1px solid #f3d6d6;
    display: flex;
    background-color: #f3d6d6;
    margin: 0 auto;

    .icon {
      width: 100%;
      font-size: 40px;
      margin: auto;
      color: #a8a8a8;
    }
  }
}

.main-input {
  .children-input {
    display: flex;
    margin-bottom: 10px;
    align-items: center;

    .input-reg {
      width: 100%;
      border-bottom: 1px solid #ffffff;
      height: 50px;
      margin-left: 10px;
      margin-top: auto;
      margin-bottom: auto;
      color: #ffffff;
    }

    .icon {
      display: flex;
      align-items: center;
      font-size: 18px;
      color: #ea2958;
    }
  }
}

.regis-socical {
  display: flex;

  .socisal-fb {
    width: 100%;

    button {
      width: 100%;
      display: flex;
      align-items: center;
      text-align: center;
      justify-content: space-between;
      border-radius: 50px;
      cursor: pointer;

      .icon {
        text-align: right;
      }

      p {
        width: 80%;
        font-weight: bold;
      }
    }
  }

  .socical-text {
    margin: auto 10px;
  }

  .socisal-gg {
    width: 100%;

    button {
      width: 100%;
      display: flex;
      align-items: center;
      text-align: center;
      justify-content: space-between;
      border-radius: 50px;
      cursor: pointer;

      .icon {
        width: 50%;
        text-align: right;
      }

      p {
        width: 80%;
        font-weight: bold;
      }
    }
  }
}
</style>
