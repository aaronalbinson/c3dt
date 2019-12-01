<template>
  <p class="paragraph">{{ ParagraphText }}</p>
</template>

<script>
export default {
  name: "Paragraph",
  props: {
    ParagraphText: String
  },
};
</script>

<style scoped>
    .paragraph {
        text-align: left;
        font-family: Arial, Helvetica, sans-serif;
    }
</style>
