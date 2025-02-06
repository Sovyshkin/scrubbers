<script>
export default {
  name: "AboutUs",
  components: {},
  data() {
    return {};
  },
  methods: {
    open() {
      try {
        this.$emit("open");
      } catch (err) {
        console.log(err);
      }
    },
  },
  mounted() {},
};
</script>
<template>
  <div class="wrapper">
    <h1>
      Официальный Дилер поломоечной техники <span class="noble">NOBLELIFT</span>
    </h1>
    <div class="wrap">
      <div class="group-img">
        <img src="../assets/card4.png" alt="" class="card" />
        <img src="../assets/glare.png" alt="" class="glare" />
      </div>
      <div class="wrap-btns">
        <div class="desc">Продажа</div>
        <div class="desc">Гарантийное обслуживание</div>
        <div class="desc">Сервисное обслуживание</div>
        <div class="desc">Запчасти</div>
        <div class="desc">Аренда</div>
        <div class="number" @click="open">Запрос стоимости</div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.wrapper {
  position: relative;
  width: 100%;
  padding: 120px 40px 30px 40px;
  background: linear-gradient(90deg, #01091d 0%, #050f2b 100%);
  display: flex;
  flex-direction: column;
  gap: 40px;
  overflow: hidden;
}

h1 {
  width: 100%;
  color: #fff;
  font-size: 50px;
  line-height: 57px;
  z-index: 2;
  text-align: center;
}

.desc {
  width: 100%;
  padding: 12px;
  background: linear-gradient(90deg, #feb803 0%, #ff9a06 100%);
  border-radius: 15px;
  color: #030a1c;
  font-weight: 400;
  font-size: 25px;
  line-height: 28px;
  transition: all 500ms ease;
  text-align: center;
  max-width: 367px;
}

.desc:hover,
.number:hover {
  cursor: pointer;
  transform: translateY(-5px);
}

.wrap-btns {
  width: 40%;
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  gap: 15px;
  z-index: 2;
}

.number {
  width: 100%;
  background-color: #dc080a;
  padding: 10px 15px;
  text-decoration: none;
  color: #fff;
  font-size: 25px;
  line-height: 28px;
  font-weight: 400;
  border-radius: 15px;
  transition: all 500ms ease;
  text-align: center;
  max-width: 367px;
}

.wrap {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background: transparent;
  z-index: 2;
}

.group-img {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
}

.glare {
  position: absolute;
  top: 55%;
  left: 40%;
  transform: translate(-50%, -50%) scale(1);
  transition: all 0.3s ease-in-out;
  z-index: -1;
  object-fit: cover;
}

.card {
  width: 70%;
  max-width: 600px;
}

.noble {
  color: rgb(227, 108, 9);
}

@media (max-width: 1500px) {
  .desc,
  .number {
    font-size: 18px;
  }
}

@media (max-width: 930px) {
  .wrapper {
    padding: 120px 10px 20px 10px;
  }

  .desc {
    padding: 7px;
  }

  .group {
    width: 100%;
  }
}

@media (max-width: 800px) {
  .wrap {
    flex-direction: column;
  }

  .wrap-btns {
    width: 80%;
  }
}

@media (max-width: 700px) {
  .desc,
  .number {
    font-size: 16px;
  }
}

@media (max-width: 500px) {
  .wrapper {
    padding-top: 110px;
  }
}
</style>
