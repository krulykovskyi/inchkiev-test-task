<template>
  <div class="final">
    <div class="final__sidebar">
      <button class="final__home-btn" />
    </div>
    <div class="final__results">
      <div class="final__results-nums">
        <div class="final__result-1">
          <p class="percents">100%</p>
          <p class="preparat">Препарат 1</p>
        </div>
        <div class="final__result-2">
          <p class="percents">100%</p>
          <p class="preparat">Препарат 2</p>
        </div>
        <div class="final__result-3">
          <p class="percents">100%</p>
          <p class="preparat">Препарат 3</p>
        </div>
      </div>
      <div class="final__title">
        <span class="your-result">Ваш результат:</span>
        <span class="your-answer">&laquo;Что я здесь делаю?&raquo;</span>
        <span class="your-description">
          Это тестовое задание, так что не будем углубляться в глубины проблем фармацевтов
        </span>
      </div>
      <button class="your-btn">
        Попробовать еще
      </button>
    </div>
    <div class="final__img-block">
      <img class="final__img" src="../../images/final-img.jpg" alt="what-am-i-doing">
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
  @import url('./FinalDisplay.css');
</style>>
