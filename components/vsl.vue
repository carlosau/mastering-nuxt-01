<script setup>
const props = defineProps({
  vslLink: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="relative" style="padding-bottom: 56.25%;">
    <iframe class="absolute top-0 left-0 w-full h-full"
      width="560"
      height="315"
      :src="props.vslLink"
      title="YouTube video player"
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      allowfullscreen
    ></iframe>
  </div>
</template>
