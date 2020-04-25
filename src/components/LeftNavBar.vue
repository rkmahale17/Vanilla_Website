<template>
  <div class="Navbar sm-d-none" v-if="isHide">
    <button type="button" class="btn-icon" @click="toggle">
      <span class="material-icons close-btn">close</span>
    </button>
    <nav class="Navbar__Items">
      <div v-for="(item,index) in menuList" :key="index" class="Navbar__Link">
        <span v-if="item.type == 'normal-link'">{{item.name}}</span>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "LeftNavBar",
  props: {
    isHide: Boolean
  },
  data: function() {
    return {
      menuList: [
        {
          name: "About",
          type: "normal-link"
        },
        {
          name: "Services",
          type: "normal-link"
        },
        {
          name: "Solution",
          type: "normal-link"
        },
        {
          name: "Blog",
          type: "normal-link"
        }
      ]
    };
  },
  methods: {
    toggle() {
      this.$emit("toggle");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/variables.scss";
.Navbar {
  background-color: #161513;
  display: flex;
  padding: 0.9em 0px;
  border-right: 1px solid gray;
  padding: 1em;
  color: white;
  z-index: 1;
  height: 500px;
  background: #4c4f49;
}
.close-btn {
  color: white;
}
.Navbar__Link {
  padding-right: 2em;
  font-size: 1em;
  color: white;
  cursor: pointer;
  font-size: 1.2em;
  padding: 10px;
  border-bottom: 1px solid gray;
}
.sm-d-none {
  display: none;
}
@media only screen and (max-width: 768px) {
  .sm-d-none {
    display: flex;
  }
}
</style>
