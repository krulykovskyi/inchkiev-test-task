<template>
  <div class="final">
    <div class="final__sidebar">
      <button class="final__home-btn" />
    </div>
    <div class="final__results">
      <div class="final__results-nums">
        <div class="final__result-1">
          <p class="percents">{{results[0]}}%</p>
          <p class="preparat">Препарат 1</p>
        </div>
        <div class="final__result-2">
          <p class="percents">{{results[1]}}%</p>
          <p class="preparat">Препарат 2</p>
        </div>
        <div class="final__result-3">
          <p class="percents">{{results[2]}}%</p>
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
  props: {
    medicamentsSales: {
      type: Object,
      required: true,
    },
  },
  mounted() {
    const salesCount = this.medicamentsSales.reduce((acc, el) => acc + el, 0);

    this.results[0] = Math.round((100 / salesCount) * this.medicamentsSales[0]);
    this.results[1] = Math.round((100 / salesCount) * this.medicamentsSales[1]);
    this.results[2] = Math.round((100 / salesCount) * this.medicamentsSales[2]);
  },
  data() {
    return {
      results: [],
    };
  },
};
</script>

<style scoped>
  @import url('./FinalDisplay.css');
</style>>
