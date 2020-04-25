<template>
  <div class="person-profile flex-box">
    <div class="perso-profile__image">
      <span class="material-icons">person_outline</span>
    </div>
    <div class="person-profile__info">
      <span class="person_name">{{personInfo.name}}</span>
      <p class="person_designation">POSITION , {{personInfo.designation}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "PersonProfile",
  props: {
    personInfo: Object
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/variables.scss";
.person-profile {
  .perso-profile__image {
    border-radius: 30px;
    width: 50px;
    height: 50px;
    border: 4px solid white;
    text-align: center;
    background: #a59494;
    line-height: 43px;
  }
  .person-profile__info {
    margin-top: 5px;
    .person_name {
      padding: 0px 0px 0px 15px;
      font-size: 1.2em;
      font-weight: 600;
    }
    .person_designation {
      color: $theme-gray;
      padding: 0px !important;
      margin: 0px 0px 0px 14px !important;
    }
  }
}
</style>
