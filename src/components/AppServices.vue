<script>
export default {
  name: "AppServices",
  components: {},
  data() {
    return {};
  },
  methods: {},
  mounted() {},
};
</script>
<template>
  <div class="wrapper">
    <h1>Услуги</h1>
    <div class="wrap-group">
      <div class="wrap-img"><img src="../assets/card4.png" alt="" /></div>
      <div class="group">
        <li class="item-group">
          <div class="listStyle"></div>
          <span>Продажа</span>
        </li>
        <li class="item-group">
          <div class="listStyle"></div>
          <span>Гарантийное обслуживание</span>
        </li>
        <li class="item-group">
          <div class="listStyle"></div>
          <span>Сервисное Обслуживание</span>
        </li>
        <li class="item-group">
          <div class="listStyle"></div>
          <span>Запчасти</span>
        </li>
        <li class="item-group">
          <div class="listStyle"></div>
          <span>Аренда</span>
        </li>
      </div>
    </div>
    <h2>Для каких объектов подходят наши машины</h2>
    <div class="group-obj">
      <span>Торгово-развлекательные центры</span>
      <span>Бизнес центры</span>
      <span>Аэровокзалы</span>
      <span>Складские помещения</span>
      <span>Медицинские учреждения</span>
      <span>Распределительные центры</span>
      <span>Паркинг</span>
      <span>Производственные помещения</span>
    </div>
  </div>
</template>
<style scoped>
.wrapper {
  width: 100%;
  padding: 20px 40px;
  display: flex;
  flex-direction: column;
  gap: 40px;
}

h1 {
  color: #fff;
  font-size: 50px;
  line-height: 57px;
  text-align: center;
}

h2 {
  text-align: center;
  font-size: 36px;
  line-height: 36px;
  color: #fff;
}

.listStyle {
  width: 9px;
  height: 9px;
  border-radius: 100%;
  background-color: #feb803;
}
.listGroup {
  display: flex;
  align-items: center;
  gap: 40px;
}

.wrap-group {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  gap: 50px;
}

.group {
  list-style: none;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  gap: 20px;
}

.wrap-img {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 239px;
  height: 300px;
}

img {
  transition: all 500ms ease;
}

img:hover {
  scale: 1.03;
}

.item-group {
  display: flex;
  align-items: center;
  gap: 10px;
}

.item-group span {
  font-size: 25px;
  line-height: 28px;
  font-weight: 400;
  color: #fff;
}

.item-group span::after,
.group-obj span::after {
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
.item-group span:hover:after,
.item-group span:focus:after,
.group-obj span:hover:after,
.group-obj span:focus:after {
  width: 100%;
}

.group-obj {
  margin: 0 auto;
  width: 70%;
  display: flex;
  align-content: center;
  justify-content: center;
  flex-wrap: wrap;
  gap: 15px;
}

.group-obj span {
  font-size: 18px;
  line-height: 18px;
  font-weight: 400;
  cursor: pointer;
  color: #fff;
}

@media (max-width: 1200px) {
  .listGroup {
    gap: 15px;
    flex-direction: column;
    align-items: start;
  }

  .group {
    gap: 15px;
  }
}

@media (max-width: 930px) {
  .wrapper {
    padding: 20px 10px;
  }
}

@media (max-width: 800px) {
  .item-group span {
    font-size: 20px;
    line-height: 20px;
  }
}

@media (max-width: 530px) {
  .wrap-group {
    flex-direction: column;
  }
}
</style>
