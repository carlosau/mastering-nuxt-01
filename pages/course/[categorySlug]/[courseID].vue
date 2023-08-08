<script setup>
import { useRoute } from "vue-router";

const route = useRoute();

const course = useCourse();
</script>

<template>
  <div>
    <p>Category is: {{ $route.params.categorySlug }}</p>
    <p>Course ID is: {{ $route.params.courseID }}</p>
    <p>{{ course.cursos[12].title }}</p>
  </div>
</template>
