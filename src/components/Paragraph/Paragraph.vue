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
        font-family: Helvetica, sans-serif;
        line-height: 24px;
        font-weight: 300;
        font-size: 14px;
        margin: 50px 0;
    }

</style>
