<script setup>
import { useRoute } from "vue-router";

//get items from courseData (start)
const route = useRoute();
const course = useCourse();
const courseItems = course.cursos;
const matchingItem = courseItems.find(item => route.params.courseID === item.slug) 
//get items from courseData (end)

//button text change (start)
const textOptions = ['comprar ahora', `por solo $${matchingItem.precio}`];
let currentTextIndex = ref(0);

const buttonText = ref(textOptions[currentTextIndex.value]);

onMounted(() => {
  setInterval(() => {
    currentTextIndex.value = (currentTextIndex.value + 1) % textOptions.length;
    buttonText.value = textOptions[currentTextIndex.value];
  }, 2000);
});
//button text change (end)

</script>

<template>
    <Head>
      <Title>Mastering Nuxt 01 </Title>
    </Head>
    <NavBar />
    <div class="p-0 bg-gray-100 w-full h-full min-h-screen flex flex-col">
      
      <div class="prose mt-20 mb-5 text-center">
        <p>div 1</p>
      </div>
  
      <div class="p-4 flex flex-col md:flex-row justify-center flex-grow space-y-4 md:space-y-0 md:space-x-4">
        <div class="prose p-6 bg-white rounded-md md:w-[30ch] md:h-[40ch] break-words">
          <p>
            Chapters(div2).................................................................
          </p>
          <p>text...</p>
        </div>
  
        <div class="prose p-6 bg-white rounded-md md:flex-1 md:w-[50ch] break-words">
          <NuxtPage />
        </div>
      </div>

      <div class="p-4 m-0 bottom-0 w-full fixed drop-shadow-lg text-center bg-white">
        <div class="flex justify-center p-2">
          <button class="bg-green-600 shadow-md rounded p-2 text-white hover:bg-green-500">{{ buttonText }}</button>
        </div>
      </div>
    </div>
  </template>