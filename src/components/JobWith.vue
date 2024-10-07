<script>
export default {
  name: "AboutUs",
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
    <h1>Работа с нами это:</h1>
    <div class="wrap-group">
      <img src="../assets/block2.png" alt="" />
      <div class="listGroup">
        <div class="group">
          <li class="item-group">
            <div class="listStyle"></div>
            <span>Гарантийное обслуживание</span>
          </li>
          <li class="item-group">
            <div class="listStyle"></div>
            <span>Продажа поломоечных машин</span>
          </li>
          <li class="item-group">
            <div class="listStyle"></div>
            <span>Аренда поломоечных машин</span>
          </li>
        </div>
        <div class="group">
          <li class="item-group">
            <div class="listStyle"></div>
            <span>Запчасти</span>
          </li>
          <li class="item-group">
            <div class="listStyle"></div>
            <span>Сервисный центр</span>
          </li>
          <li class="item-group">
            <div class="listStyle"></div>
            <span>Оперативная работа</span>
          </li>
        </div>
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
  text-align: center;
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
  gap: 40px;
}

img {
  transform: rotate(90deg);
  width: 239px;
  height: 359px;
  object-fit: cover;
  border-radius: 15px;
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

.item-group span::after {
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
.item-group span:focus:after {
  width: 100%;
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
  img {
    width: 200px;
    height: 200px;
  }

  .item-group span {
    font-size: 20px;
    line-height: 20px;
  }
}

@media (max-width: 530px) {
  .wrap-group {
    flex-direction: column;
  }

  img {
    width: 270px;
    height: 270px;
  }
}
</style>
