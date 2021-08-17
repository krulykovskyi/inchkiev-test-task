<template>
  <!-- <div>
    <button @click="addLike">Like</button>
    <button @click="addDislike">Dislike</button>
  </div>
  <div>
    count of likes: <strong>{{ likes }}</strong>
  </div>
  <div>
    count of dislikes: <strong>{{ dislikes }}</strong>
  </div> -->
  <PostForm
    @create="createPost"
  />
  <PostList
    :posts="posts"
  />
  <CoverDisplay />
  <MainDisplay />
  <FinalDisplay />
</template>

<script>
import PostForm from './components/PostForm.vue';
import PostList from './components/PostList.vue';
import CoverDisplay from './components/CoverDisplay/CoverDisplay.vue';
import MainDisplay from './components/MainDisplay/MainDisplay.vue';
import FinalDisplay from './components/FinalDisplay/FinalDisplay.vue';

export default {
  components: {
    PostForm,
    PostList,
    CoverDisplay,
    MainDisplay,
    FinalDisplay,
  },
  data() {
    return {
      posts: [
        { id: 1, title: 'JavaScript', body: 'info about this post' },
        { id: 2, title: 'C++', body: 'info about this post' },
        { id: 3, title: 'Python', body: 'info about this post' },
      ],
      title: '',
      body: '',
    };
  },
  methods: {
    createPost(post) {
      this.posts.push(post);
    },
  },
};
</script>

<style>
  @font-face {
    font-family: 'AvenirNextCyr-Bold';
    src: url('./fonts/avenirnextcyr-bold.ttf') format('truetype');
  }
  @font-face {
    font-family: 'AvenirNextCyr-Demi';
    src: url('./fonts/avenirnextcyr-demi.ttf') format('truetype');
  }
  @font-face {
    font-family: 'AvenirNextCyr-Heavy';
    src: url('./fonts/avenirnextcyr-heavy.ttf') format('truetype');
  }
  @font-face {
    font-family: 'AvenirNextCyr-Light';
    src: url('./fonts/avenirnextcyr-light.ttf') format('truetype');
  }
  @font-face {
    font-family: 'AvenirNextCyr-Medium';
    src: url('./fonts/avenirnextcyr-medium.ttf') format('truetype');
  }
  @font-face {
    font-family: 'AvenirNextCyr-Regular';
    src: url('./fonts/avenirnextcyr-regular.ttf') format('truetype');
  }
  @font-face {
    font-family: 'AvenirNextCyr-Thin';
    src: url('./fonts/avenirnextcyr-thin.ttf') format('truetype');
  }
  @font-face {
    font-family: 'AvenirNextCyr-UltraLight';
    src: url('./fonts/avenirnextcyr-ultralight.ttf') format('truetype');
  }

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'AvenirNextCyr-Bold';
  }
</style>
