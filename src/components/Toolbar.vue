<template>
  <div class="toolbar">

    <div class="Navbar">
      <div class="Navbar__Link Navbar__Link-toggle">
        <button type="button" class="btn-icon" @click="toggle">
          <span class="material-icons">menu</span>
        </button>
      </div>
      <div class="Navarbar__Logo">
        COMPONY
        <span>LOGO</span>
      </div>
      <div class="Navbar__Link Navbar__Link-toggle align-end">
        <span class="material-icons">message</span>
      </div>

      <nav class="Navbar__Items Navbar__Items--right">
        <div v-for="(item,index) in menuList" :key="index" class="Navbar__Link">
          <span v-if="item.type == 'normal-link'">{{item.name}}</span>
          <button v-else class="getInTouchButton">
            <span class="material-icons">message</span>
            <span>Get In Touch</span>
          </button>
        </div>
      </nav>
      
    </div>
        <LeftNavBar :isHide="isHide" @toggle="toggle"/>
  </div>
</template>

<script>
import LeftNavBar from "./LeftNavBar";
export default {
  name: "Toolbar",
  components: {
    LeftNavBar
  },
  data: function() {
    return {
      isHide: false,
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
        },
        {
          name: "Blog",
          type: "get-in-touch-button"
        }
      ]
    };
  },
  methods: {
    toggle() {
      this.isHide = !this.isHide;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/variables.scss";
.Navarbar__Logo {
  padding-left: 0.8em;
  font-size: 1.2em;
  font-weight: 500;
  span {
    color: $theme-red;
  }
}
.Navbar {
  background-color: $them-black;
  display: flex;
  color: $theme-gray;
  padding: 0.9em 0px;
}

.Navbar__Link {
  padding-right: 2em;
  span {
    color: $theme-gray;
    cursor: pointer;
  }
}
.Navbar__Link:hover {
  padding-right: 2em;
  span {
    color: white;
    cursor: pointer;
  }
}

.Navbar__Items {
  display: flex;
}

.Navbar__Items--right {
  margin-left: auto;
}

.Navbar__Link-toggle {
  display: none;
}

.getInTouchButton {
  background: $theme-red;
  padding: 0.8px;
  font-size: 0.9em;
  width: 140px;
  border-radius: 20px;
  border: 1px solid $theme-red;
  margin-top: -10px;
  span {
    padding-right: 0.3em;
    font-size: 1.2em;
    color: white !important;
  }
}

@media only screen and (max-width: 768px) {
  .Navbar__Items,
  .Navbar {
    flex-direction: column;
  }
  .align-end {
    align-self: flex-end !important;
  }
  .Navbar__Items {
    display: none;
  }

  .Navbar__Items--right {
    margin-left: 0;
  }

  .Navbar__ToggleShow {
    display: flex;
  }

  .Navbar__Link-toggle {
    align-self: flex-start;
    display: initial;
    position: absolute;
    cursor: pointer;
    padding-left: 10px;
  }
  .Navarbar__Logo {
    display: flex;
    align-self: center;
    padding-left: 0.8em;
    font-size: 1.2em;
    font-weight: 500;
    span {
      color: $theme-red;
    }
  }
}
</style>
