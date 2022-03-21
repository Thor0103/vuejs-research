<template>
  <div class="header">
    <ul>
      <li>
        <router-link class="link" to="/">
          <Icon type="fas" key-name="faHouse" />
          Trang chủ
        </router-link>
      </li>
      <li>
        <router-link class="link" to="/login">
          <Icon type="far" key-name="faCalendarAlt" />
          Đăng nhập
        </router-link>
      </li>
      <li>
        <router-link class="link" to="/register">
          <Icon type="fab" key-name="faAccusoft" />
          Đăng ký
        </router-link>
      </li>
    </ul>
  </div>
  <div class="main">
    <router-view />
  </div>
  <div></div>
</template>

<script>
import Icon from "@/components/Icon";

export default {
  name: "Layout",
  components: {
    Icon,
  },
};
</script>

<style scoped lang="scss">
@import "src/assets/scss/variable";

.header {
  font-family: "Josefin Sans", sans-serif;
}

.header ul {
  display: flex;
  list-style: none;
}

.header ul li {
  text-decoration: none;
  flex: 1;
  justify-content: space-between;
  align-items: center;
  text-align: center;
}

.link {
  text-decoration: none;
  font-weight: bold;
}
</style>
