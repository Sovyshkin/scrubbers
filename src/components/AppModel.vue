<script>
export default {
  name: "AppModel",
  components: {},
  data() {
    return {
      cards: [
        {
          name: "NB380",
          items: [
            {
              name: "Ширина водосборной балки",
              value: "430 мм",
            },
            {
              name: "Рабочая ширина захвата",
              value: "380 мм",
            },
            {
              name: "Мощность двигателя вращения щетки",
              value: "380 Вт",
            },
            {
              name: "Мощность двигателя всасывания",
              value: "150 Вт",
            },
            {
              name: "Масса (без АКБ)",
              value: "58.5 кг",
            },
            {
              name: "Скорость вращения щётки",
              value: "180 об/мин",
            },
            {
              name: "Уровень шума",
              value: "65±3 dB",
            },
            {
              name: "Ёмкость бака раствора",
              value: "10 л",
            },
            {
              name: "Ёмкость бака грязной воды",
              value: "10 л",
            },
            {
              name: "Высота",
              value: "120 см",
            },
            {
              name: "Ширина",
              value: "43 см",
            },
            {
              name: "Длина",
              value: "70 см",
            },
          ],
          active: false,
          img: "card5",
          new: true,
        },
        {
          name: "NB530",
          items: [
            {
              name: "Диаметр дисковой щетки",
              value: "530 мм",
            },
            {
              name: "Рабочая ширина водосборной балки",
              value: "760 мм",
            },
            {
              name: "Объем бака для чистой воды",
              value: "50 л",
            },
            {
              name: "Объем бака для грязной воды",
              value: "50 л",
            },
            {
              name: "Производительность",
              value: "1800 м/ч",
            },
            {
              name: "Время непрервыной работы",
              value: "3-4 ч",
            },
            {
              name: "Мощность двигателя вращения щетки",
              value: "550 Вт",
            },
            {
              name: "Мощность двигателя всасывания",
              value: "400 Вт",
            },
            {
              name: "Уровень шума",
              value: "65±3 dB",
            },
            {
              name: "Напряжение питания",
              value: "2х12/100 В/Ач",
            },
            {
              name: "Масса (без АКБ)",
              value: "89 кг",
            },
          ],
          active: false,
          img: "card1",
        },
        {
          name: "NR530",
          active: false,
          items: [
            {
              name: "Диаметр дисковой щетки",
              value: "530 мм",
            },
            {
              name: "Рабочая ширина водосборной балки",
              value: "760 мм",
            },
            {
              name: "Объем бака для чистой воды",
              value: "70 л",
            },
            {
              name: "Объем бака для грязной воды",
              value: "70 л",
            },
            {
              name: "Производительность",
              value: "3100 м/ч",
            },
            {
              name: "Время непрервыной работы",
              value: "3-4 ч",
            },
            {
              name: "Мощность двигателя вращения щетки",
              value: "550 Вт",
            },
            {
              name: "Мощность двигателя всасывания",
              value: "550 Вт",
            },
            {
              name: "Мощность тягового двигателя",
              value: "400 Вт",
            },
            {
              name: "Скорость движения",
              value: "0-6 км/ч",
            },
            {
              name: "Уровень шума",
              value: "68±3 dB",
            },
            {
              name: "Напряжение питания",
              value: "2х12/120 В/Ач",
            },
            {
              name: "Масса (без АКБ)",
              value: "120 кг",
            },
            {
              name: "Габаритные размеры",
              value: "1260х600х1010 мм",
            },
          ],
          img: "card2",
        },
        {
          name: "NR810",
          items: [
            {
              name: "Диаметр дисковой щетки",
              value: "410х2 мм",
            },
            {
              name: "Рабочая ширина водосборной балки",
              value: "810 мм",
            },
            {
              name: "Объем бака для чистой воды",
              value: "120 л",
            },
            {
              name: "Объем бака для грязной воды",
              value: "120 л",
            },
            {
              name: "Производительность",
              value: "4860 м/ч",
            },
            {
              name: "Время непрервыной работы",
              value: "3-4 ч",
            },
            {
              name: "Мощность двигателя вращения щетки",
              value: "380х2 Вт",
            },
            {
              name: "Мощность двигателя всасывания",
              value: "500 Вт",
            },
            {
              name: "Мощность тягового двигателя",
              value: "650 Вт",
            },
            {
              name: "Скорость движения",
              value: "0-6 км/ч",
            },
            {
              name: "Уровень шума",
              value: "68±3 dB",
            },
            {
              name: "Напряжение питания",
              value: "4х6/200 В/Ач",
            },
            {
              name: "Масса (без АКБ)",
              value: "195 кг",
            },
            {
              name: "Габаритные размеры",
              value: "1415х890х1120 мм",
            },
          ],
          active: false,
          img: "card3",
        },
        {
          name: "NR1060",
          items: [
            {
              name: "Диаметр дисковой щетки",
              value: "530х2 мм",
            },
            {
              name: "Рабочая ширина водосборной балки",
              value: "1115 мм",
            },
            {
              name: "Объем бака для чистой воды",
              value: "200 л",
            },
            {
              name: "Объем бака для грязной воды",
              value: "210 л",
            },
            {
              name: "Производительность",
              value: "6890 м/ч",
            },
            {
              name: "Время непрервыной работы",
              value: "5-6 ч",
            },
            {
              name: "Мощность двигателя вращения щетки",
              value: "550х2 Вт",
            },
            {
              name: "Мощность двигателя всасывания",
              value: "600 Вт",
            },
            {
              name: "Мощность тягового двигателя",
              value: "800 Вт",
            },
            {
              name: "Скорость движения",
              value: "0-6,5 км/ч",
            },
            {
              name: "Уровень шума",
              value: "68±3 dB",
            },
            {
              name: "Напряжение питания",
              value: "36В В/Ач",
            },
            {
              name: "Масса (без АКБ)",
              value: "340 кг",
            },
            {
              name: "Габаритные размеры",
              value: "1800х1150х1350 мм",
            },
          ],
          active: false,
          img: "card4",
        },
      ],
      active: false,
    };
  },
  methods: {},
  mounted() {},
};
</script>
<template>
  <div class="wrapper">
    <h1>Модельный ряд</h1>
    <div class="cards">
      <div
        class="card"
        @click="card.active = !card.active"
        v-for="card in cards"
        :key="card.name"
      >
        <img v-if="card.new" src="../assets/new.png" alt="" class="new" />
        <img class="card-img" :src="'../assets/' + card.img + '.png'" alt="" />
        <div class="name">{{ card.name }}</div>
        <div class="group" v-if="!card.active">
          <div
            class="item-group"
            v-for="item in card.items.slice(0, 5)"
            :key="item.name"
          >
            <p class="item-name">{{ item.name }}</p>
            <span class="item-value">{{ item.value }}</span>
          </div>
          <div class="wrap-arrow">
            <a class="number" href="tel: 8(3532) 30-77-17">Запрос стоимости</a>
            <img class="arrow" src="../assets/arrow-down.png" alt="" />
          </div>
        </div>
        <div class="group" v-else>
          <div class="item-group" v-for="item in card.items" :key="item.name">
            <p class="item-name">{{ item.name }}</p>
            <span class="item-value">{{ item.value }}</span>
          </div>
          <div class="wrap-arrow">
            <a class="number" href="tel: 8(3532) 30-77-17">Запрос стоимости</a>
            <img class="arrow top" src="../assets/arrow-down.png" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.wrapper {
  width: 100%;
  padding: 10px 40px;
  background: linear-gradient(90deg, #01091d 0%, #050f2b 100%);
  display: flex;
  flex-direction: column;
  gap: 40px;
  border-radius: 50px;
}

h1 {
  text-align: center;
  color: #fff;
  font-size: 50px;
  line-height: 57px;
}

.cards {
  margin: 0 auto;
  display: flex;
  gap: 10px;
  flex-wrap: wrap;
}

.card {
  flex: 19%;
  display: flex;
  min-height: 530px;
  flex-direction: column;
  gap: 20px;
  background-color: #fff;
  border: 2px solid #fff;
  border-radius: 10px;
  padding: 15px 15px 100px 15px;
  transition: all 500ms ease;
  position: relative;
}

.card:hover {
  border: 2px solid #feb803;
  transform: translateY(-5px);
}

.card-img {
  height: 20vh;
  margin: 0 auto;
  object-fit: cover;
}

.name {
  font-size: 25px;
  line-height: 28px;
  color: #050f2a;
  font-weight: 700;
  text-align: center;
}

.item-name,
.item-value {
  font-size: 13px;
  line-height: 15px;
  color: #050f2a;
  font-weight: 400;
}

.group {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.item-group {
  display: flex;
  align-items: center;
  gap: 10px;
  justify-content: space-between;
}

.item-value {
  text-align: right;
}
.wrap-arrow {
  width: 100%;
  position: absolute;
  bottom: 1%;
  left: 50%;
  transform: translate(-50%);
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  gap: 10px;
}

.arrow {
  transition: all 500ms ease;
}
.top {
  transform: rotate(180deg);
}

.number {
  background-color: #dc080a;
  padding: 7px 12px;
  text-decoration: none;
  color: #fff;
  font-size: 16px;
  line-height: 15px;
  font-weight: 400;
  border-radius: 10px;
  transition: all 500ms ease;
}

.new {
  position: absolute;
  width: 40px;
  height: 40px;
}
@media (max-width: 930px) {
  .wrapper {
    padding: 20px 10px;
  }
}

@media (max-width: 480px) {
  .cards {
    flex-direction: column;
  }
}
</style>
