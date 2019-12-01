<template>
  <h2 class="subHeader">{{ SubHeaderText }}</h2>
</template>

<script>
export default {
  name: "SubHeader",
  props: {
    SubHeaderText: String
  },
};
</script>

<style scoped>
    .subHeader {
        text-align: left;
    }
</style>
