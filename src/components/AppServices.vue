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
      <div class="wrap-img"><img src="../assets/block2.jpg" alt="" /></div>
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
        <h2 class="clin">Клининг</h2>
        <div class="group-items">
          <li class="desc">
            Комплексное обслуживание коммерческой недвижимости
          </li>
          <li class="desc">Мойка окон и витражей</li>
          <li class="desc">Уборка после строительства</li>
        </div>
      </div>
      <div class="group-obj">
        <h2>Аренда поломоечных машин</h2>
        <div class="group-items">
          <li class="desc">
            Аренда поломоечных машин на сутки и длительный срок
          </li>
        </div>
      </div>
      <div class="group-obj">
        <h2 class="ser">Сервисное обслуживание</h2>
        <div class="group-items">
          <li class="desc">
            Ремонт и техническое обслуживание поломоечных машин
          </li>
        </div>
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
  width: fit-content;
  text-align: center;
  font-size: 24px;
  line-height: 28px;
  color: #fff;
}

h2::after {
  margin-top: 2px;
  background-color: rgb(
    227,
    108,
    9
  ); /* Цвет линии при наведении на нее курсора мыши */
  display: block;
  content: "";
  height: 2px; /* Высота линии */
  width: 100%;
  -webkit-transition: width 0.3s ease-in-out;
  -moz--transition: width 0.3s ease-in-out;
  transition: width 0.3s ease-in-out;
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
  width: 330px;
  transition: all 500ms ease;
  object-fit: cover;
  border-radius: 15px;
}

img:hover {
  scale: 1.03;
}

.group-items {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.item-group {
  flex: 48%;
  display: flex;
  align-items: center;

  text-align: center;
  gap: 10px;
}

.item-group span {
  width: fit-content;
  font-size: 19px;
  line-height: 22px;
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
  width: 33%;
  display: flex;
  flex-direction: column;
  gap: 15px;
  align-items: center;
}

.wrap-items {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.services {
  width: 90%;
  display: flex;
  gap: 20px;
  margin: 0 auto;
  align-items: start;
  justify-content: space-between;
}

.desc {
  width: 100%;
  padding: 12px;
  background: linear-gradient(90deg, #feb803 0%, #ff9a06 100%);
  border-radius: 15px;
  color: #030a1c;
  font-weight: 400;
  font-size: 18px;
  line-height: 26px;
  transition: all 500ms ease;
  text-align: center;
  max-width: 367px;
  list-style: none;
}

.desc:hover,
.number:hover {
  cursor: pointer;
  transform: translateY(-5px);
}

@media (max-width: 1200px) {
  .services {
    width: 100%;
  }

  .clin {
    padding-right: 80px;
  }
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
    align-items: center;
  }

  .clin,
  .ser {
    padding-right: 0;
  }

  .group-obj {
    width: 100%;
    align-items: center;
  }
}

@media (max-width: 530px) {
  .wrap-group {
    flex-direction: column;
  }

  h2 {
    width: 100%;
  }
}
</style>
