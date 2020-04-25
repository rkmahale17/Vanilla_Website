<template>
  <div id="testimonials">
    <h2 class="text-center">Testimonials</h2>
    <div class="flex-horizontal_spacearound">
      <div class="testimonials_box box-arrow__bottom">
        <div>
          <span class="material-icons rotate180 format_quote_icon">format_quote</span>
          Lorem Ipsum is simply dummy text of the printing and typesetting industry.
        </div>
        <PersonProfile :personInfo="personInfo1" class="person_profile"/>
      </div>
      <div class="testimonials_box box-arrow__bottom">
        <div>
          <span class="material-icons rotate180 format_quote_icon">format_quote</span>
          scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic.
        </div>
        <PersonProfile :personInfo="personInfo2" class="person_profile"/>
      </div>
      <div class="testimonials_box box-arrow__bottom">
        <div>
          <span class="material-icons rotate180 format_quote_icon">format_quote</span>
          Contrary to popular belief, Lorem Ipsum is not simply random text.
        </div>
        <PersonProfile :personInfo="personInfo3" class="person_profile"/>
      </div>
    </div>
  </div>
</template>

<script>
import PersonProfile from "./PersonProfile";
export default {
  name: "Testimonials",
  components: {
    PersonProfile
  },
  data: function() {
    return {
      personInfo1: {
        name: "Steve M",
        designation: "Jr Developer"
      },
      personInfo2: {
        name: "Michel S",
        designation: "Sr Tester"
      },
      personInfo3: {
        name: "Shane W",
        designation: "Project Owner"
      }
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/variables.scss";
#testimonials {
  background: #d6d6d6;
  padding: 2em 0px;
}

.testimonials_box {
  height: fit-content;
  border-radius: 10px;
  margin: 4% 2% 100px 2%;
  padding: 3% 2%;
  width: 300px;
  background: white;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.19), 0 6px 6px rgba(0, 0, 0, 0.23);
}
.box-arrow__bottom:after {
  content: " ";
  position: absolute;
  margin: 2.6% 0% 0% 10%;
  border-top: 16px solid white;
  border-right: 16px solid transparent;
  border-left: 16px solid #c29a9a00;
  transform: rotate(-4 deg);
}

.format_quote_icon {
  color: $theme-red;
  display: inline-flex;
  position: relative;
  left: 8px;
  top: -8px;
}
.person_profile {
  position: absolute;
  margin: 3em 0% 0% 3%;
}
</style>
