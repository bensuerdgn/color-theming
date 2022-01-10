<template>
  <div class="theme-mode-container">
    <div class="theme-toggle" @click="showbar = !showbar">
      <i class="fas fa-palette"></i>
    </div>
    <div class="theme-bar" v-if="showbar">
      <label class="switch">
        <input type="checkbox" @click="toggleTheme" />
        <span class="slider round"></span>
      </label>
      <label for="color">
        <input
          type="color"
          id="favcolor"
          name="favcolor"
          v-model="colorPicker"
        />
      </label>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return { showbar: false, theme: "", colorPicker: "" };
  },
  watch: {
    colorPicker: function (val) {
      var root = document.documentElement;
      root.style.setProperty("--background-color", val);
      root.style.setProperty("--text-color", "white");
    },
  },
  methods: {
    toggleTheme() {
      this.theme = this.theme == "darkMode" ? "" : "darkMode"; //toggles theme value
      document.documentElement.setAttribute("data-theme", this.theme); // sets the data-theme attribute
      localStorage.setItem("theme", this.theme); // stores theme value on local storage
    },
  },
  mounted() {
    let localTheme = localStorage.getItem("theme"); //gets stored theme value if any
    document.documentElement.setAttribute("data-theme", localTheme); // updates the data-theme attribute
  },
};
</script>

<style>
</style>