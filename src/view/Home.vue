<template>
  <div class="home-container">
    <Header />
    <Section />
    <ThemeMode/>
    <Footer />
  </div>
</template>

<script>
import Header from "../components/Header";
import Section from "../components/Section";
import ThemeMode from "../components/ThemeMode";
import Footer from "../components/Footer";

export default {
  components: {
    Header,
    Section,
    ThemeMode,
    Footer,
  },
};
</script>

<style lang="scss">
@import "@/scss/style.scss";

</style>