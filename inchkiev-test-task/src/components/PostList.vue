<template>
  <div>
    <h2>Cgbcjr gjcnjd</h2>
    <PostItem
      v-for="post in posts" :key="post.id"
      :post="post"
    />
  </div>
</template>

<script>
import PostItem from './PostItem.vue';

export default {
  components: {
    PostItem,
  },
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
</style>
