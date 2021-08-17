<template>
  <div class="main">
    <div class="main__sidebar">
      <div class="main__sidebar-buttons">
        <button class="main__home-button"></button>
        <button class="main__reload-button"></button>
      </div>
      <div class="main__params">
        <h3 class="main__params-text">Параметры:</h3>
        <div class="main__counters">
          <div class="main__sad-counter">
            <img class="counter-img" src="../../images/sad_icon.svg" alt="">
            <span>15</span>
          </div>
          <div class="main__happy-counter">
            <img class="counter-img" src="../../images/happy_icon.svg" alt="">
            <span>15</span>
          </div>
          <div class="main__heart-counter">
            <img class="counter-img" src="../../images/heart_icon.svg" alt="">
            <span>15</span>
          </div>
        </div>
      </div>
      <div class="main__sidebar-queue-info">
        <p class="main__sidebar-queue-text">Осталось в очереди:</p>
        <p class="main__sidebar-queue-numbers">
          <strong>14</strong>
          /15
        </p>
      </div>
    </div>
    <div class="main__game">
      <div class="main__patient-card">
        <img class="main__patient-photo" src="../../images/image.jpg" alt="patient">
        <span class="main__patient-info">
          <p class="main__patient-name">Валентина, 75 років</p>
          <p class="main__patient-text">
            Дитя, дай бабусі ліки від тиску за цим рецептом, але не дорогих, тих, що дешевші!
          </p>
        </span>
      </div>
       <div class="main__medications-btns">
        <button class="main__med-btn-1">
          Препарат 1
        </button>
        <button class="main__med-btn-2">
          Препарат 2
        </button>
        <button class="main__med-btn-3">
          Препарат 3
        </button>
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
};
</script>

<style scoped>
  @import url('./MainDisplay.css');
</style>
