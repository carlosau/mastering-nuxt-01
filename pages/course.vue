<template>
    <Head>
      <Title>Mastering Nuxt 01 </Title>
    </Head>
    <div class="p-6 bg-gray-100 w-full h-full min-h-screen flex flex-col">
      
      <div class="prose mb-12">
        <p>div 1</p>
      </div>
  
      <div class="flex flex-col md:flex-row justify-center flex-grow space-y-4 md:space-y-0 md:space-x-4">
        <div class="prose p-8 bg-white rounded-md md:w-[30ch] md:h-[40ch] break-words">
          <p>
            Chapters(div2).................................................................
          </p>
          <p>text...</p>
        </div>
  
        <div class="prose p-8 bg-white rounded-md md:flex-1 md:w-[50ch] break-words">
          <NuxtPage />
        </div>
      </div>
    
    </div>
  </template>