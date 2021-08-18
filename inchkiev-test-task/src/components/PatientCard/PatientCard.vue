<template>
  <div class="patient-card">
    <img class="patient-card__photo" :src="personPhoto" alt="patient">
    <span class="patient-card__info">
      <p class="patient-card__name">{{ patient.name}}</p>
      <p class="patient-card__text">
        {{patient.text}}
      </p>
    </span>
  </div>
</template>

<script>
import Mariya from '../../images/Mariya.jpg';
import Stepan from '../../images/Stepan.jpg';
import Lubov from '../../images/Lubov.jpg';
import Alexandr from '../../images/Alexandr.jpg';
import Iruna from '../../images/Iruna.jpg';

const photos = [Mariya, Stepan, Lubov, Alexandr, Iruna];

export default {

  props: {
    patient: {
      type: Object,
      required: true,
    },
    patientIndex: {
      type: Number,
      required: true,
    },
  },
  beforeUpdate() {
    this.personPhoto = photos[this.patientIndex];
  },
  data() {
    return {
      personPhoto: photos[this.patientIndex],
      animation: false,
    };
  },
};
</script>

<style scoped>
  @import url('./PatientCard.css');
</style>
