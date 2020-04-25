<template>
  <div class="contact-us">
    <p class="text-center contact-us__header1">Convienced To Work With Us ?</p>
    <p
      class="text-center contact-us__header2"
    >Compony Has Helped agencies keep their promises to client since 2005</p>

    <div class="contact-us__forms">
      <div class="flex-horizontal_center sm-block">
        <section class="pl-5">
          <input class="custome_input" type="text" placeholder="Fullname">
        </section>
        <section class="pl-5">
          <input class="custome_input" type="text" placeholder="Email Adreess">
        </section>
        <section class="pl-5">
          <input class="custome_input" type="text" placeholder="Phone No">
        </section>
      </div>
      <div class="flex-horizontal_center sm-block">
        <section class="pl-5">
          <textarea class="custome_textarea" placeholder="Message in brief"/>
        </section>
      </div>
      <div class="flex-horizontal_center">
        <button class="btn-submit">Submit</button>
      </div>
    </div>
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
.contact-us {
  display: block;
  color: white;
  background: #252524;
  padding: 3%;
}
.contact-us__header1 {
  font-size: 1.5em;
  margin-bottom: 10px;
}
.contact-us__header2 {
  margin-top: 0px !important;
}
.btn-submit {
  border: 2px solid #f03b00;
  background: #f03b00;
  padding: 7px 26px;
  color: white;
  font-size: 1em;
  border-radius: 17px;
  margin-top: 10px;
}
</style>
