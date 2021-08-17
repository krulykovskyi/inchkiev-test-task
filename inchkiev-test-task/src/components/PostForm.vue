<template>
  <form @submit.prevent>
    <h4>Create post</h4>
    <input
      v-model="post.title"
      class="input"
      type="text"
      placeholder="name of post"
    />
    <input
      v-model="post.body"
      class="input"
      type="text"
      placeholder="body of post"
    />
    <button class="btn" @click="createPost">create</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: '',
        body: '',
      },
    };
  },
  methods: {
    createPost() {
      this.post.id = new Date().toDateString();
      this.$emit('create', this.post);
      this.post = {
        title: '',
        body: '',
      };
    },
  },
};
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.input {
  width: 100%;
  border: 2px solid green;
  padding: 10px;
}

.btn {
  align-self: flex-end;
  width: 80px;
  height: 50px;
}
</style>
