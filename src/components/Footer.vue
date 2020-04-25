<template>
  <div class="footer flex-end sm-block">
    <section>
      <span>&copy; 2017 Compony. All rights are reserved.</span>
    </section>
    <section class="mt-10 pl-10">
      Follow Us On :
      <img
        class="footer__social-icons"
        src="https://img.icons8.com/material/24/000000/facebook-new.png"
      >
      <img
        class="footer__social-icons"
        src="https://img.icons8.com/material/24/000000/linkedin.png"
      >
      <img
        class="footer__social-icons"
        src="https://img.icons8.com/material/24/000000/twitter-squared.png"
      >
      <img
        class="footer__social-icons"
        src="https://img.icons8.com/material/24/000000/filled-message--v1.png"
      >
    </section>
  </div>
</template>

<script>
export default {
  name: "Footer"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/variables.scss";
.footer {
  display: flex;
  background: black;
  height: 80px;
  color: $theme-gray;
  font-size: 0.8em;
  padding: 2em;
}
.footer__social-icons {
  background: white;
  margin: 5px 0px -8px 10px;
  cursor: pointer;
}
</style>
