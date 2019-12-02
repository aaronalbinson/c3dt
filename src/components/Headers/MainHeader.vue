<template>
  <h1 class="mainHeader">{{ MainHeaderText }}</h1>
</template>

<script>
export default {
  name: "MainHeader",
  props: {
    MainHeaderText: String
  },
};
</script>

<style scoped>
  @import url('https://fonts.googleapis.com/css?family=Prata&display=swap');
  .mainHeader {
      font-family: 'Prata', serif;
      font-size: 48px;
      line-height: 50px;
      margin-left: 70px;
      display: inline;

  }
  .mainHeader::before {
    content: " ";
    width: 60px;
    height: 1px;
    background-color: #000;
    display: inline-block;
    margin-right: 10px;
    margin-bottom: 18px;
    margin-left: -70px;
  }
</style>
