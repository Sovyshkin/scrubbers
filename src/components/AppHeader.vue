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
    <div class="wrap-logo">
      <img class="logo" src="../assets/logo.png" alt="" />
      <span>ОФИЦИАЛЬНЫЙ ДИЛЕР ПОЛОМОЕЧНОЙ ТЕХНИКИ <b>NOBLELIFT</b></span>
    </div>
    <nav class="group">
      <li class="nav-item" @click="scrollTo('aboutus')">О компании</li>
      <li class="nav-item" @click="scrollTo('services')">Услуги</li>
      <li class="nav-item" @click="scrollTo('model')">Модельный ряд</li>
      <li class="nav-item" @click="scrollTo('contacts')">Контакты</li>
      <a href="https://vk.com/noblelift_oren" target="_blank"
        ><img class="vk" src="../assets/vk.png" alt=""
      /></a>
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
  justify-content: space-between;
  gap: 10px;
  background: linear-gradient(90deg, #01091d 0%, #050f2b 100%);
  z-index: 3;
}

.group {
  display: flex;
  align-items: center;
  gap: 20px;
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

.wrap-logo {
  display: flex;
  align-items: center;
  gap: 15px;
}

.wrap-logo span {
  font-size: 12px;
  line-height: 12px;
  text-align: center;
  color: #fff;
}

.wrap-logo span b {
  color: rgb(227, 108, 9);
}

.logo {
  max-height: 200px;
  max-width: 200px;
}

.vk {
  height: 40px;
  width: 40px;
}

@media (max-width: 1200px) {
  .wrapper {
    flex-direction: column;
  }
}

@media (max-width: 700px) {
  .wrap-logo {
    gap: 8px;
  }
  .logo {
    max-width: 150px;
    max-height: 150px;
  }

  .nav-item {
    font-size: 14px;
    line-height: 14px;
    text-align: center;
  }
}

@media (max-width: 500px) {
  .wrapper {
    padding: 10px;
  }
  .group {
    gap: 7px;
  }

  .nav-item {
    font-size: 12px;
    line-height: 12px;
    text-align: center;
  }

  .vk {
    height: 30px;
    height: 30px;
    object-fit: cover;
  }
}
</style>
