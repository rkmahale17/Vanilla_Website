<template>
  <div class="body-menu">
    <div id="body-menu__message">
      <span>Carrots or drink an entire arc enforcement</span>
    </div>
    <div class="flex-horizontal_center services-menu">
      <div v-for="(item,index) in serviceMenu" :key="index" class="sm-d-flex body-menu__serviceBox">
        <section class="body-menu__icon">
          <span class="material-icons">{{item.icon}}</span>
        </section>
        <section class="body-menu__service-name">{{item.name}}</section>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BodyMenu",
  data: function() {
    return {
      serviceMenu: [
        {
          name: "Cloud Messaging",
          icon: "message"
        },
        {
          name: "Cloud Storage",
          icon: "cloud"
        },
        {
          name: "Auth 2.0",
          icon: "lock"
        }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/variables.scss";
.body-menu {
  background: black;
  min-height: 70vh;
}
.body-menu__service-name {
  font-size: 0.8em;
  margin-top: 8%;
}

#body-menu__message {
  margin: auto;
  padding: 5vh 10px;
  color: white;
  text-align: center;
  max-width: 400px;
  font-size: 2em;
}
.body-menu__icon {
  margin-top: 10%;
  span {
    font-size: 3em;
    color: $theme-red;
  }
}
.services-menu {
  margin-top: 5%;
}
.body-menu__serviceBox {
  cursor: pointer;
  border: 1px solid #424040;
  width: 150px;
  height: 120px;
  color: white;
  text-align: center;
  vertical-align: middle;
  margin: 0.5em 1em;
}
</style>
