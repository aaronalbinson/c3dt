<template>
  <div id="card">
    <SubHeader SubHeaderText="Sub-heading title" />
    <MainHeader MainHeaderText="Main title sits here" />
    <Paragraph
      ParagraphText="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam non urna eu augue maximus aliquam. Pellentesque sit amet lobortis sapien. Nullam maximus nibh id maximus vestibulum. Donec sit amet fringilla tellus, vel ultrices justo. Phasellus ornare turpis quis augue maximus mattis augue."
    />
    <CallToAction CallToActionText="Call to action" CallToActionLink="https://google.com" />
  </div>
</template>

<script>
import SubHeader from "../Headers/SubHeader.vue";
import MainHeader from "../Headers/MainHeader.vue";
import Paragraph from "../Paragraph/Paragraph.vue";
import CallToAction from "../CallToAction/CallToAction.vue";

export default {
  name: "Card",
  props: {
    SubHeaderText: String,
    MainHeaderText: String,
    ParagraphText: String,
    CallToActionText: String,
    CallToActionLink: String
  },
  components: {
    SubHeader,
    MainHeader,
    Paragraph,
    CallToAction
  }
};
</script>

<style>
#card {
  max-width: 500px;
  padding: 20px;
}

@media only screen and (min-width: 700px) {
  #card {
      margin-left: 90px;
  }
}

@media only screen and (min-width: 1000px) {
  #card {
      margin-left: 150px;
  }
}
</style>
