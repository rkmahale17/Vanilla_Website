<template>
  <div id="app">
    <Toolbar/>
    <BodyMenu/>
    <PeopleConnect/>
    <Testimonials/>
    <ContactUs/>
    <Footer/>
  </div>
</template>

<script>
import Toolbar from "./components/Toolbar";
import BodyMenu from "./components/BodyMenu";
import PeopleConnect from "./components/PeopleConnect";
import Testimonials from "./components/Testimonials";
import Footer from "./components/Footer";
import ContactUs from "./components/ContactUs";

export default {
  name: "App",
  components: {
    Toolbar,
    BodyMenu,
    PeopleConnect,
    Testimonials,
    Footer,
    ContactUs
  }
};
</script>

<style lang="scss">
@import "./assets/main.scss";
@import "./assets/medias.scss";
</style>
