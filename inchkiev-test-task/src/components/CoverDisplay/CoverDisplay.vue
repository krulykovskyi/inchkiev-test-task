<template>
  <div class="cover">
    <div class="cover__background">
      <div class="cover__circle">
        <div class="cover__circle-content">
          <h4 class="cover__greetings">Добро пожаловать в игру</h4>
          <h1 class="cover__game-name">Помоги <br> ФАРМАЦЕВТУ</h1>
          <button
            @click="startGame"
            class="cover__start-btn"
          >
            Начать
          </button>
        </div>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  data() {
    return {
    };
  },
  methods: {
    startGame() {
      this.$emit('start');
    },
  },
};
</script>

<style scoped>
  @import url('./CoverDisplay.css');
</style>>
