<template>
  <a class="callToAction" :href="CallToActionLink">{{ CallToActionText }} <svg width="7" height="11" fill="none" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" clip-rule="evenodd" d="M2.463.625C3.81 2.327 5.215 4.041 6.375 5.5c-1.366 1.702-2.739 3.41-3.912 4.875H.375L4.3 5.5.376.625h2.087z" fill="#000"/></svg></a>
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
        font-family: Helvetica, sans-serif;
        font-weight: 400;
        font-size: 16px;
        text-transform: uppercase;
        color: #000;
        text-decoration: none;
    }
    .callToAction svg {
        margin-left: 5px;
    }
</style>
