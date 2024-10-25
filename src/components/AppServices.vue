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
    <h1>Для каких объектов подходят наши машины</h1>
    <div class="wrap-group">
      <div class="wrap-img"><img src="../assets/block2.jpeg" alt="" /></div>
      <div class="group">
        <li class="item-group">
          <div class="listStyle"></div>
          <span>торгово-развлекательные центры</span>
        </li>
        <li class="item-group">
          <div class="listStyle"></div>
          <span>бизнес центры</span>
        </li>
        <li class="item-group">
          <div class="listStyle"></div>
          <span>медицинские учреждения</span>
        </li>
        <li class="item-group">
          <div class="listStyle"></div>
          <span>аэровокзалы</span>
        </li>
        <li class="item-group">
          <div class="listStyle"></div>
          <span>распределительные центры</span>
        </li>
        <li class="item-group">
          <div class="listStyle"></div>
          <span>складские помещения</span>
        </li>
        <li class="item-group">
          <div class="listStyle"></div>
          <span>производственные помещения</span>
        </li>
        <li class="item-group">
          <div class="listStyle"></div>
          <span>паркинг</span>
        </li>
      </div>
    </div>
    <h1>Услуги</h1>
    <div class="services">
      <div class="group-obj">
        <h2>Клининг</h2>
        <div class="wrap-items">
          <li class="item-group">
            <div class="listStyle"></div>
            <span>Комплексное обслуживание коммерческой недвижимости</span>
          </li>
          <li class="item-group">
            <div class="listStyle"></div>
            <span>Мойка окон и витражей</span>
          </li>
          <li class="item-group">
            <div class="listStyle"></div>
            <span>Уборка после строительства</span>
          </li>
        </div>
      </div>
      <div class="group-obj">
        <h2>Аренда поломоечных машин</h2>
        <li class="item-group">
          <div class="listStyle"></div>
          <span>Аренда поломоечных машин на сутки и длительный срок</span>
        </li>
      </div>
      <div class="group-obj">
        <h2>Сервисное обслуживание</h2>
        <li class="item-group">
          <div class="listStyle"></div>
          <span>Ремонт и техническое обслуживание поломоечных машин</span>
        </li>
      </div>
    </div>
  </div>
</template>
<style scoped>
.wrapper {
  width: 100%;
  padding: 20px 40px 20px 40px;
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
  font-size: 30px;
  line-height: 32px;
  color: #fff;
}

.listStyle {
  min-width: 9px;
  min-height: 9px;
  max-width: 9px;
  max-height: 9px;
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
  width: 60%;
  list-style: none;
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  gap: 20px;
}

.wrap-img {
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 15px;
}

img {
  width: 359px;
  height: 302px;
  transition: all 500ms ease;
  object-fit: cover;
  border-radius: 15px;
}

img:hover {
  scale: 1.03;
}

.item-group {
  flex: 48%;
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

.group-obj {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 15px;
}

.wrap-items {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.services {
  display: flex;
  gap: 20px;
  justify-content: space-between;
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

  .item-group span {
    font-size: 20px;
    line-height: 20px;
    font-weight: 400;
    color: #fff;
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

  .services {
    flex-direction: column;
    gap: 20px;
  }

  .group-obj {
    align-items: center;
  }
}

@media (max-width: 530px) {
  .wrap-group {
    flex-direction: column;
  }
}
</style>
