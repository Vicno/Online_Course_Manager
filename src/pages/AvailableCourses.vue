<template>
  <div>
    <CoursesCard v-for="course in courses" :key="course.name" v-bind="course" />
  </div>
</template>

<script>
import { defineComponent } from "vue";
import CoursesCard from "src/components/CoursesCard.vue";
import courses from "src/store/courses";

export default defineComponent({
  name: "AvailableCourses",
  components: {
    CoursesCard,
  },
});
</script>
