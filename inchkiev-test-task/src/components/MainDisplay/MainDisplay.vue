<template>
  <div class="main">
    <div class="main__sidebar">
      <div class="main__sidebar-buttons">
        <button
          @click="this.$emit('restart')"
          class="main__home-button"
        />
        <button
          @click="this.$emit('restart')"
          class="main__reload-button"
        />
      </div>
      <div class="main__params">
        <h3 class="main__params-text">Параметры:</h3>
        <div class="main__counters">
          <div class="main__sad-counter">
            <img class="counter-img" src="../../images/sad_icon.svg" alt="">
            <span>{{medicamentsSales[0]}}</span>
          </div>
          <div class="main__happy-counter">
            <img class="counter-img" src="../../images/happy_icon.svg" alt="">
            <span>{{medicamentsSales[1]}}</span>
          </div>
          <div class="main__heart-counter">
            <img class="counter-img" src="../../images/heart_icon.svg" alt="">
            <span>{{medicamentsSales[2]}}</span>
          </div>
        </div>
      </div>
      <div class="main__sidebar-queue-info">
        <p class="main__sidebar-queue-text">Осталось в очереди:</p>
        <p class="main__sidebar-queue-numbers">
          <strong>{{queue.length - patient.id}}</strong>
          /{{queue.length}}
        </p>
      </div>
    </div>
    <div class="main__game">
      <PatientCard
        :patient="patient"
        :patientIndex="patientIndex"
      />
      <div class="main__medications-btns">
        <button
          @click="sale(0)"
          class="main__med-btn-1">
          Препарат 1
        </button>
        <button
          @click="sale(1)"
          class="main__med-btn-2">
          Препарат 2
        </button>
        <button
          @click="sale(2)"
          class="main__med-btn-3">
          Препарат 3
        </button>
      </div>
    </div>
  </div>

</template>

<script>
import PatientCard from '../PatientCard/PatientCard.vue';

export default {
  components: {
    PatientCard,
  },
  props: {
    queue: {
      type: Array,
      required: true,
    },
    medicamentsSales: {
      type: Object,
      required: true,
    },
  },
  data() {
    const patientIndex = 0;

    return {
      patientIndex,
      patient: this.queue[patientIndex],
    };
  },
  methods: {
    sale(num) {
      this.$emit('sale', num);

      const salesCount = this.medicamentsSales.reduce((acc, el) => acc + el, 0);

      if (salesCount === this.queue.length) {
        this.$emit('end');
      }

      this.patientIndex += 1;
      this.patient = this.queue[this.patientIndex];
    },
  },
};
</script>

<style scoped>
  @import url('./MainDisplay.css');
</style>
