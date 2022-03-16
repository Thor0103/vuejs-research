<template>
  <div class="header">
    <ul>
      <li>
        <router-link to="/">Trang chu</router-link>
      </li>
      <li>
        <router-link to="/login">Dang nhap</router-link>
      </li>
      <li>
        <router-link to="/register">Dang ky</router-link>
      </li>
    </ul>
  </div>
  <div class="main">
    <router-view />
  </div>
  <div></div>
</template>

<script>
export default {
  name: "Layout",
};
</script>
