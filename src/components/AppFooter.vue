<script>
export default {
  name: "AppFooter",
  components: {},
  data() {
    return {
      navs: [
        {
          name: "О нас",
          value: "aboutus",
        },
        {
          name: "Услуги",
          value: "services",
        },
        {
          name: "Контакты",
          value: "contacts",
        },
        {
          name: "Мы на карте",
          value: "contacts",
        },
      ],
      contacts: [
        "8 (3532) 30-77-17",
        "8 (9325) 54-44-04",
        "E-mail: r89058196314@yandex.ru",
        "Адрес: Г Оренбург, ул Монтажников, 23, 1 этаж, место П14",
      ],
      products: [
        "Продажа поломоечных машин",
        "Гарантийное обслуживание",
        "Сервисный центр",
        "Запчасти",
        "Аренда поломоечных машин",
      ],
    };
  },
  methods: {
    scrollTo(name) {
      const element = document.getElementById(name);
      if (element) {
        window.scrollTo({ top: element.offsetTop - 90, behavior: "smooth" });
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
      <span class="logo">NOBLELIFTOREN</span>
      <div class="wrap-items">
        <li
          class="nav-item"
          @click="scrollTo(item.value)"
          v-for="item in navs"
          :key="item.name"
        >
          {{ item.name }}
        </li>
      </div>
    </nav>
    <div class="products">
      <h3>Продукция и услуги:</h3>
      <div class="wrap-product">
        <div class="product" v-for="item in products" :key="item">
          {{ item }}
        </div>
      </div>
    </div>
    <div class="contacts">
      <h3>Контакты</h3>
      <div class="wrap-contacts">
        <div class="contact">
          <a href="tel: 8(3532) 30-77-17" class="item-group"
            >8(3532) 30-77-17</a
          >
        </div>
        <div class="contact">
          <a href="tel: 8 (9325) 54-44-04" class="item-group"
            >8 (9325) 54-44-04</a
          >
        </div>
        <div class="contact">E-mail: r89058196314@yandex.ru</div>
        <div class="contact">
          Адрес: Г Оренбург, ул Монтажников, 23, 1 этаж, место П14
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  margin-top: 100px;
  width: 100%;
  padding: 20px 40px;
  display: flex;
  justify-content: space-evenly;
  gap: 25px;
  background-color: #030a1c;
}

h3 {
  color: #ffffff;
  font-weight: 700;
  font-size: 15px;
  line-height: 17px;
}

.logo {
  font-size: 25px;
  color: #fff;
  font-weight: 700;
  line-height: 28px;
}

.group,
.contacts,
.wrap-contacts,
.wrap-items,
.wrap-product,
.products {
  display: flex;
  flex-direction: column;
  gap: 5px;
  list-style-type: none;
}

.nav-item,
.contact,
.product {
  font-weight: 400;
  font-size: 15px;
  line-height: 17px;
  color: #fff;
  width: fit-content;
  cursor: pointer;
}

a {
  font-weight: 400;
  font-size: 15px;
  line-height: 17px;
  color: #fff;
  width: fit-content;
  cursor: pointer;
  text-decoration: none;
}

.logo-polic {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.text-polic {
  font-weight: 400;
  font-size: 21px;
  line-height: 21px;
  color: #fff;
  cursor: pointer;
  width: fit-content;
}

.nav-item::after,
.contact::after,
.text-polic::after,
.product::after {
  margin-top: 1px;
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
.nav-item:focus:after,
.contact:focus::after,
.contact:hover::after,
.text-polic:focus::after,
.text-polic:hover::after,
.product:focus::after,
.product:hover::after {
  width: 100%;
}
@media (max-width: 930px) {
  .wrapper {
    padding: 20px 10px;
  }
}

@media (max-width: 800px) {
  h3 {
    font-size: 20px;
    line-height: 20px;
  }

  .nav-item,
  .contact,
  .text-polic,
  .product {
    font-size: 14px;
    line-height: 14px;
  }
}

@media (max-width: 738px) {
  .wrapper {
    flex-direction: column;
    align-items: center;
  }

  .group,
  .contacts,
  .products {
    align-items: center;
    text-align: center;
  }

  .wrap-contacts,
  .wrap-items,
  .wrap-product {
    width: 80%;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
  }

  .logo-polic {
    align-items: center;
    justify-content: center;
    gap: 15px;
  }
}

@media (max-width: 450px) {
  .logo {
    height: 60px;
    width: auto;
  }
}
</style>
