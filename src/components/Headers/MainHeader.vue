<template>
  <div class="mainHeader">
    <h1 class="mainHeaderText">{{ MainHeaderText }}</h1>
  </div>
</template>

<script>
export default {
  name: "MainHeader",
  props: {
    MainHeaderText: String
  }
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css?family=Prata&display=swap");
.mainHeader {
  max-width: 400px;
}
.mainHeaderText {
  font-family: "Prata", serif;
  font-size: 48px;
  line-height: 50px;
  margin-left: 70px;
  display: inline;
}
.mainHeaderText::before {
  content: " ";
  width: 60px;
  height: 1px;
  background-color: #000;
  display: inline-block;
  margin-right: 10px;
  margin-bottom: 18px;
  margin-left: -70px;
}
@media only screen and (min-width: 1000px) {
  .mainHeader {
    max-width: 500px;
  }
  .mainHeaderText {
    font-size: 64px;
    line-height: 68px;
  }
}
</style>
