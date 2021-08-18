<template>
  <div class="patient-card">
        <img class="patient-card__photo" src="../../images/Valentina.jpg" alt="patient">
        <span class="patient-card__info">
          <p class="patient-card__name">Валентина, 75 років</p>
          <p class="patient-card__text">
            Дитя, дай бабусі ліки від тиску за цим рецептом, але не дорогих, тих, що дешевші!
          </p>
        </span>
      </div>
</template>

<script>
export default {
  props: {
    patient: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {};
  },
};
</script>

<style scoped>
  @import url('./PatientCard.css');
</style>
