<template>
  <div>
    <Layout>
      <Tags />
      <Notes />
      <Types />
      <NumberPad />
    </Layout>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Tags from "@/components/Money/Tags.vue";
import Notes from "@/components/Money/Notes.vue";
import Types from "@/components/Money/Types.vue";
import NumberPad from "@/components/Money/NumberPad.vue";
export default Vue.extend({
  name: "Money",
  components: {
    Tags,
    Notes,
    Types,
    NumberPad,
  },
});
</script>

<style lang="scss" scoped>
@import "~@/assets/styles/colo.scss";
@import "~@/assets/styles/helper.scss";

.selected {
  color: $color-highlight;
}

p {
  color: $red;
}
</style>
