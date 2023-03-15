<template>
  <div class="rounded-b-lg bg-white text-center">
    <div
      class="bg-image h-96 w-auto"
      :style="'background-image: url(' + featuredPost.image + ');'"
    ></div>
    <div class="p-4">
      <div class="flex place-items-center justify-center">
        <h3 class="pr-2">{{ featuredPost.tagline }}</h3>
        <img src="/play-button.svg" height="30px" />
      </div>
      <h2>{{ featuredPost.title }}</h2>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    featuredPost: {
      type: Object,
      default: () => {},
    },
  },
};
</script>
