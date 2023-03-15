<template>
  <div class="rounded-b-lg bg-white text-center">
    <div
      class="bg-image h-60 w-auto"
      :style="'background-image: url(' + post.image + ');'"
    ></div>
    <div class="p-4">
      <h3 class="pb-2">{{ post.tagline }}</h3>
      <h2>{{ post.title }}</h2>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      default: () => {},
    },
  },
};
</script>
