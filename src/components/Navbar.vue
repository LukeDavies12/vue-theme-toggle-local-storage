<template>
  <div class="navbar">
    <div class="container">
      <nav>
        <div class="nav-left">
          <router-link to="/">
            <h3>Vue Theme Toggle with Local Storage</h3>
          </router-link>
        </div>
        <div class="nav-right">
          <router-link to="/">Home</router-link>
          <router-link to="/about">About</router-link>
          <ToggleTheme/>
        </div>
      </nav>
    </div>
  </div>
</template>

<script>
import ToggleTheme from "@/components/ToggleTheme.vue";
export default {
  components: {
    ToggleTheme
  }
};
</script>

<style lang="scss" scoped>
.navbar {
  nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
    .nav-right {
      display: flex;
      align-items: center;
      justify-content: space-between;
      a {
        margin-left: 30px;
      }
      .toggletheme {
        margin-left: 30px;
      }
    }
  }
}
</style>