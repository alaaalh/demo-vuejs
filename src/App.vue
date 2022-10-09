<template>
  <store-resource :storedResources='storedResources'></store-resource>
</template>

<script>
import StoreResource from './components/learning-resources/StoreResource.vue'
export default {
  components: {
    StoreResource,
  },
  data() {
    return {
      storedResources: [
        {
          id: "official_gide",
          title: "Official Gide",
          description: "this is the official vue decumantaion",
          link: "http://vuejs.org",
        },
        {
          id: "google",
          title: "Google",
          description: "Learn to google...",
          link: "http://google.org",
        },
      ],
    };
  },
};
</script>
