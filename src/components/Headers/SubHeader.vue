<template>
  <h2 class="subHeader">{{ SubHeaderText }}</h2>
</template>

<script>
export default {
  name: "SubHeader",
  props: {
    SubHeaderText: String
  }
};
</script>

<style scoped>
.subHeader {
  font-family: Helvetica, sans-serif;
  font-weight: 300;
  font-size: 18px;
}
@media only screen and (min-width: 1000px) {
  .subHeader {
    font-size: 24px;
  }
}
</style>
