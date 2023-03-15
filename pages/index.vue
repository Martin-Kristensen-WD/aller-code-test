<template>
  <div>
    <div class="my-4 bg-primaryRed">
      <h1 class="p-4">SKÆBNER</h1>
    </div>
    <div class="mx-3 grid grid-cols-6">
      <div class="col-span-6 lg:col-span-5 lg:max-w-5xl">
        <div class="mb-4 grid grid-cols-6 gap-4 lg:mr-6">
          <div class="col-span-6">
            <FeaturedPost :featuredPost="featuredPost" />
          </div>
          <div
            v-for="post in posts"
            :key="post.id"
            class="col-span-6 lg:col-span-3"
          >
            <SmallPost :post="post" />
          </div>
        </div>
      </div>
      <div class="col-span-6 lg:col-span-1 lg:mr-4">
        <AdPost />
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    const posts = ref([]);
    const featuredPost = ref({});

    /* Fetch data when the page mounts */
    onMounted(async () => {
      const response = await fetch("http://localhost:3000/posts");
      posts.value = await response.json();
      featuredPost.value = posts.value.shift(); // Use the first index of posts as featured post (large)
    });

    return {
      posts,
      featuredPost,
    };
  },
};
</script>
