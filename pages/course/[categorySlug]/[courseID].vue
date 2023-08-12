<script setup>
import { useRoute } from "vue-router";

const route = useRoute();

const course = useCourse();

const courseItems = course.cursos;

const returnIDfromRoute = (() => {
  const matchingItemFn = courseItems.find(item => route.params.courseID === item.slug) 
  return console.log(matchingItemFn ? matchingItemFn.id : 'Not Found')
}) 

const matchingItem = courseItems.find(item => route.params.courseID === item.slug) 

</script>

<template>
  <div>
    <p>Category is: {{ $route.params.categorySlug }}</p>
    <p>Course route is: {{ $route.params.courseID }}</p>
    <p>The ID of this route is: {{ matchingItem.id }}</p>
    <p>Title is: {{ matchingItem.title }}</p>
    <p class="text-orange-500"><button class="bg-green-400 text-white p-2" @click="returnIDfromRoute()">show ID in Console</button></p>
    <vsl
    :vslLink="matchingItem.vsl" 
    />
    <h2 class="font-bold">About</h2>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Architecto saepe consequuntur quaerat quas delectus quisquam ipsum error, eius, veritatis corporis distinctio at ducimus harum a recusandae dignissimos, magni facere amet?</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Architecto saepe consequuntur quaerat quas delectus quisquam ipsum error, eius, veritatis corporis distinctio at ducimus harum a recusandae dignissimos, magni facere amet?</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Architecto saepe consequuntur quaerat quas delectus quisquam ipsum error, eius, veritatis corporis distinctio at ducimus harum a recusandae dignissimos, magni facere amet?</p>
  </div>
</template>
