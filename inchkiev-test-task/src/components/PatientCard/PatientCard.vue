<template>
  <div class="patient-card">
        <img class="patient-card__photo" :src="patient.imgUrl" alt="patient">
        <span class="patient-card__info">
          <p class="patient-card__name">{{ patient.name}}</p>
          <p class="patient-card__text">
            {{patient.text}}
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
