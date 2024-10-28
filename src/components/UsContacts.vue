<script>
import AppMap from "./AppMap.vue";
export default {
  name: "AboutUs",
  components: { AppMap },
  data() {
    return {};
  },
  methods: {},
  mounted() {},
};
</script>
<template>
  <div class="wrapper">
    <h1>Контакты</h1>
    <div class="wrap">
      <div class="info">
        <div class="group">
          <span class="item-group main">Адрес:</span>
          <span class="item-group"
            >Г Оренбург, ул Монтажников, 23, 1 этаж, офис П14</span
          >
        </div>
        <div class="group">
          <span class="item-group main">Телефон:</span>
          <div class="group-phone">
            <a href="tel: +73532307717" class="item-group">8(3532) 30-77-17</a>
            <a href="tel: +79325544404" class="item-group">8(9325) 54-44-04</a>
          </div>
        </div>
        <div class="group">
          <span class="item-group main">E-mail:</span>
          <span class="item-group">oren-service@yandex.ru</span>
        </div>
        <div class="group">
          <span class="item-group main">Время работы:</span>
          <span class="item-group">пн-пт с 9:00 до 18:00</span>
        </div>
      </div>
      <div class="wrap-map">
        <AppMap />
      </div>
    </div>
  </div>
</template>
<style scoped>
.wrapper {
  width: 100%;
  padding: 10px 40px;
  display: flex;
  flex-direction: column;
  gap: 40px;
}

h1 {
  color: #fff;
  font-size: 50px;
  line-height: 57px;
  width: fit-content;
  padding-bottom: 10px;
  border-bottom: 3px solid #feb803;
}

.wrap {
  width: 100%;
  display: flex;
  align-items: stretch;
  gap: 20px;
}

.group {
  display: flex;
  align-items: center;
  gap: 10px;
}

.info {
  background: linear-gradient(90deg, #feb803 0%, #ff9a06 100%);
  padding: 30px;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  gap: 15px;
  border-radius: 15px;
}

.info,
.wrap-map {
  flex: 50%;
}

.wrap-map {
  overflow: hidden;
  height: 36.5vh;
  border-radius: 15px;
}

.item-group {
  font-size: 25px;
  line-height: 28px;
  font-weight: 400;
  color: #fff;
}

.main {
  font-weight: 700;
}

.item-group::after {
  margin-top: 2px;
  background-color: #fff; /* Цвет линии при наведении на нее курсора мыши */
  display: block;
  content: "";
  height: 2px; /* Высота линии */
  width: 0%;
  -webkit-transition: width 0.3s ease-in-out;
  -moz--transition: width 0.3s ease-in-out;
  transition: width 0.3s ease-in-out;
}
.item-group:hover:after,
.item-group:focus:after {
  width: 100%;
}

.group-phone {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

@media (max-width: 1200px) {
  .info {
    gap: 10px;
    padding: 15px;
  }

  .item-group {
    font-size: 20px;
    line-height: 20px;
  }
}

@media (max-width: 930px) {
  .wrapper {
    padding: 20px 10px;
  }
}

@media (max-width: 850px) {
  .wrap {
    flex-direction: column;
  }
}

@media (max-width: 480px) {
  .item-group {
    font-size: 16px;
    line-height: 16px;
  }

  .info {
    gap: 8px;
  }
}
</style>
