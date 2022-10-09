<template>
  <ul>
    <learning-resources
      v-for="res in storedResources"
      :key="res.id"
      :title="res.title"
      :description="res.description"
      :link="res.link"
    ></learning-resources>
  </ul>
</template>

<script>
import LearningResources from "./LearningResourcesItem.vue";
export default {
  props: ["storedResources"],
  components: {
    LearningResources,
  },
};
</script>
