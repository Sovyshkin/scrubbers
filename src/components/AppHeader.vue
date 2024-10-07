<script>
export default {
  name: "AppHeader",
  components: {},
  data() {
    return {
      menu: false,
    };
  },
  methods: {
    scrollTo(name) {
      const element = document.getElementById(name);
      if (element) {
        window.scrollTo({ top: element.offsetTop, behavior: "smooth" });
      } else {
        location.reload();
      }
    },
  },
  mounted() {},
};
</script>

<template>
  <div class="wrapper">
    <nav class="group">
      <li class="nav-item" @click="scrollTo('aboutus')">О нас</li>
      <li class="nav-item" @click="scrollTo('services')">Услуги</li>
      <li class="nav-item" @click="scrollTo('contacts')">Контакты</li>
      <li class="nav-item" @click="scrollTo('contacts')">Филиалы</li>
    </nav>
  </div>
</template>

<style scoped>
.wrapper {
  position: fixed;
  width: 100%;
  padding: 10px 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(90deg, #01091d 0%, #050f2b 100%);
  z-index: 3;
}

.group {
  display: flex;
  align-items: center;
  gap: 40px;
  transition: all 400ms ease;
}
.nav-item {
  font-size: 18px;
  font-weight: 400;
  line-height: 18px;
  color: #fff;
  list-style-type: none;
  cursor: pointer;
}

.nav-item::after {
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
.nav-item:hover:after,
.nav-item:focus:after {
  width: 100%;
}

@media (max-width: 500px) {
  .wrapper {
    padding: 10px;
  }
  .group {
    gap: 15px;
  }

  .nav-item {
    font-size: 14px;
  }
}
</style>
