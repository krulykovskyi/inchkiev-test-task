<template>
  <div class="post" :key="post.id">
    <div><strong>Title: </strong>{{post.title}}</div>
    <div><strong>Body: </strong> {{post.body}}</div>
    <div>
      <button @click="deletePost(post.id)">
        delete post
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
  .post {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 15px;
    border: 2px solid yellowgreen;
    margin-top: 15px;
  }
</style>
