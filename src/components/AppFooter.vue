<script>
export default {
  name: "AppFooter",
  components: {},
  data() {
    return {
      navs: [
        {
          name: "О компании",
          value: "aboutus",
        },
        {
          name: "Услуги",
          value: "services",
        },
        {
          name: "Модельный ряд",
          value: "model",
        },
        {
          name: "Контакты",
          value: "contacts",
        },
      ],
      contacts: [
        "8(3532) 30-77-17",
        "8(9325) 54-44-04",
        "E-mail: oren-service@yandex.ru",
        "Адрес: Г Оренбург, ул Монтажников, 23, 1 этаж, офис П14",
      ],
      products: [
        "Продажа поломоечной техники",
        "Комплексное обслуживание коммерческой недвижимости",
        "Мойка окон и витражей",
        "Уборка после строительства",
        "Аренда поломоечных машин на сутки и длительный срок",
        "Ремонт и техническое обслуживание поломоечных машин",
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
      <div class="wrap-logo">
        <img class="logo" src="../assets/logo.png" alt="" />
        <span>ОФИЦИАЛЬНЫЙ ДИЛЕР ПОЛОМОЕЧНОЙ ТЕХНИКИ <b>NOBLELIFT</b></span>
      </div>
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
          <a href="tel: +73532307717" class="item-group">+7 (3532) 30-77-17</a>
        </div>
        <div class="contact">
          <a href="tel: +79325544404" class="item-group">+7-932-554-44-04</a>
        </div>
        <div class="contact">E-mail: oren-service@yandex.ru</div>
        <div class="contact">
          Адрес: г Оренбург, ул Монтажников, 23, 1 этаж, офис П14
        </div>
        <div class="contact">
          Сайт: <a href="https://чистыйсервис.online/">чистыйсервис.online</a>
        </div>
        <a href="https://vk.com/noblelift_oren" target="_blank"
          ><img class="vk" src="../assets/vk.png" alt=""
        /></a>
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
  width: fit-content;
  color: #ffffff;
  font-weight: 700;
  font-size: 15px;
  line-height: 17px;
}

.wrap-logo {
  display: flex;
  align-items: center;
  flex-direction: column;
  gap: 7px;
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
  max-height: 140px;
  max-width: 140px;
}

.contacts,
.products {
  padding-top: 53px;
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

.vk {
  height: 40px;
  width: 40px;
}

h3::after {
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
    padding-top: 0;
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
