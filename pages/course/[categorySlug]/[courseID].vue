<script setup>
import { useRoute } from "vue-router";

const route = useRoute();
</script>

<template>
  <div>
    <p>Category is: {{ $route.params.categorySlug }}</p>
    <p>Course ID is: {{ $route.params.courseID }}</p>
  </div>
</template>
