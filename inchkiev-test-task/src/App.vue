<template>
  <CoverDisplay
    v-if="!isGameStarted"
    @start="startGame"
  />
  <MainDisplay
    v-else-if="isGameStarted && !isGameEnded"
    @sale="sale"
    :queue="queue"
    :medicamentsSales="medicamentsSales"
    @end="endGame"
  />
  <FinalDisplay
    v-else
    :medicamentsSales="medicamentsSales"
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
          id: 1,
          name: 'Марія, 19 років',
          text: 'Бабуся приймає брендовий препарат від болю в суглобах, він допомагає, але занадто дорогий. У Вас є якісний аналог з нижчою ціною? Якщо ні — давайте бренд.',
          imgUrl: '../../images/Mariya.jpg',
        },
        {
          id: 2,
          name: 'Степан, 61 рік',
          text: 'Спросоння відсунув гарячий чайник рукою та обпікся. У Вас всі ліки від опіків такі дорогі? Можна хороший препарат недорого?',
          imgUrl: '../../images/Stepan.jpg',
        },
        {
          id: 3,
          name: 'Любов, 58 років',
          text: 'Лікар призначив препарат від артеріальної гіпертензії, а бренд дорого коштує. Тому мені потрібен аналог з хорошою ефективністю та приємною ціною.',
          imgUrl: '../../images/Lubov.jpg',
        },
        {
          id: 4,
          name: 'Олександр, 20 років',
          text: 'Порекомендуйте ефективний препарат від болю в горлі за розумну ціну.',
          imgUrl: '../../images/Alexandr.jpg',
        },
        {
          id: 5,
          name: 'Ірина, 55 років',
          text: 'У мене часто невралгії, лікар призначив вітаміни групи В. Мені потрібен якісний аналог за прийнятною ціною.',
          imgUrl: '../../images/Iruna.jpg',
        },
      ],
      isGameStarted: false,
      isGameEnded: false,
      medicamentsSales: [0, 0, 0],
    };
  },

  methods: {
    startGame() {
      this.isGameStarted = true;
    },

    endGame() {
      this.isGameEnded = true;
    },

    sale(num) {
      this.medicamentsSales[num] += 1;
    },
  },
};
</script>

<style>
  @import url('./App.css');
</style>
