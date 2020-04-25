<template>
  <div class="people-connect flex-horizontal_spacearound">
    <div class="people-connect__main">
      <p
        class="people-connect__header_text"
      >Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old.</p>
      <p
        class="people-connect__main_text"
      >Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat</p>
    </div>
    <div class="people-connect__main">
      <img src="../assets/map.jpg" alt="Internet Image ">
    </div>
  </div>
</template>

<script>
export default {
  name: "PeopleConnect"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/variables.scss";
.people-connect__header_text {
  font-weight: 500;
  font-size: 1.4em;
}
.people-connect__main_text {
  font-size: 1.2em;
}
.people-connect__main {
  padding: 3% 2%;
  max-width: 500px;
  img {
    width: 100%;
    height: auto;
  }
}
</style>
