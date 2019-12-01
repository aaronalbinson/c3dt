<template>
  <a class="callToAction" :href="CallToActionLink">{{ CallToActionText }}</a>
</template>

<script>
export default {
  name: "CallToAction",
  props: {
    CallToActionText: String,
    CallToActionLink: String
  },
};
</script>

<style scoped>
    .callToAction {
        text-align: left;
        font-family: Arial, Helvetica, sans-serif;
    }
</style>
