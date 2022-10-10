<template>
  <!-- <store-resource :storedResources='storedResources'></store-resource>
  <details-forms></details-forms> -->
  <student-menu></student-menu>
</template>

<script>
// import StoreResource from './components/learning-resources/StoreResource.vue'
// import DetailsForms from './components/Forms/details-forms.vue'
import StudentMenu from './components/StudentMenu/student-menu.vue'
export default {
  components: {
    // StoreResource,
    // DetailsForms,
    StudentMenu
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
