<template>
  <CoverDisplay
    v-if="!isGameStarted"
    @start="startGame"
  />
  <MainDisplay
    v-else
    @end="endGame"
    :queue="queue"
  />
  <FinalDisplay
    v-if="isGameEnded"
  />
</template>

<script>
import CoverDisplay from './components/CoverDisplay/CoverDisplay.vue';
import MainDisplay from './components/MainDisplay/MainDisplay.vue';
import FinalDisplay from './components/FinalDisplay/FinalDisplay.vue';

export default {
  components: {
    CoverDisplay,
    MainDisplay,
    FinalDisplay,
  },
  data() {
    return {
      queue: [
        {
          id: 1, name: '', text: '', imgUrl: '',
        },
        {
          id: 2, name: '', text: '', imgUrl: '',
        },
        {
          id: 3, name: '', text: '', imgUrl: '',
        },
        {
          id: 4, name: '', text: '', imgUrl: '',
        },
        {
          id: 5, name: '', text: '', imgUrl: '',
        },
      ],
      isGameStarted: false, //+
      isGameEnded: false,
    };
  },
  methods: {
    startGame() {
      this.isGameStarted = true;
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
