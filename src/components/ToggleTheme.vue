<template>
  <div class="toggletheme">
    <button
      role="button"
      aria-label="Toggle dark/light"
      @click.prevent="toggleTheme"
      class="toggle-theme"
    >
      <ion-icon v-if="darkTheme" name="sunny"></ion-icon>
      <ion-icon v-else name="ios-moon"></ion-icon>
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      darkTheme: false
    };
  },
  methods: {
    toggleTheme() {
      this.darkTheme = !this.darkTheme;
      // This is using a script that is added in index.html
      window.__setPreferredTheme(this.darkTheme ? "dark" : "light");
    }
  },
  mounted() {
    if (window.__theme == "dark") this.darkTheme = true;
  }
};
</script>

<style lang="scss" scoped>
.toggle-theme{
    background: transparent;
    padding: 5px 5px;
    cursor: pointer;
    ion-icon{
        font-size: 21px;
    }
}
</style>