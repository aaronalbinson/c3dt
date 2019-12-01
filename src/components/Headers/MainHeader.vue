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
    .mainHeader {
        text-align: left;
        font-family: Arial, Helvetica, sans-serif;
    }
</style>
