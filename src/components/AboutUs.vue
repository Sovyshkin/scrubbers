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
    <h1>Поломоечные машины: чистота и комфорт вашего пространства</h1>
    <img src="../assets/block1.png" alt="" />
    <div class="wrap-desc">
      <div class="left">
        <div class="desc">Быстро и эффективно</div>
        <div class="desc">Современные технологии</div>
      </div>
      <div class="right">
        <div class="desc">Удобство использования</div>
        <div class="desc">Экономия времени и труда</div>
      </div>
    </div>
    <div class="wrap-btns">
      <a class="number" href="tel: 8(3532) 30-77-17">Запрос стоимости</a>
    </div>
  </div>
</template>
<style scoped>
.wrapper {
  position: relative;
  width: 100%;
  padding: 110px 40px 30px 40px;
  background: linear-gradient(90deg, #01091d 0%, #050f2b 100%);
  display: flex;
  flex-direction: column;
  gap: 40px;
}

.wrapper2 {
  border-radius: 0 0 50px 50px;
  width: 100%;
  padding: 40px 40px 20px 40px;
  background: linear-gradient(90deg, #01091d 0%, #050f2b 100%);
  display: flex;
  flex-direction: column;
  gap: 40px;
}

h1 {
  width: 80%;
  color: #fff;
  font-size: 50px;
  line-height: 57px;
  z-index: 2;
}

img {
  position: absolute;
  width: 70%;
  height: auto;
  top: 65%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.wrap-desc {
  padding-top: 250px;
  margin: 0 auto;
  width: 80%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  z-index: 2;
}

.left,
.right {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 40px;
}

.desc {
  width: fit-content;
  padding: 12px;
  background: linear-gradient(90deg, #feb803 0%, #ff9a06 100%);
  border-radius: 15px;
  color: #030a1c;
  font-weight: 400;
  font-size: 25px;
  line-height: 28px;
  transition: all 500ms ease;
}

.desc:hover,
.number:hover {
  cursor: pointer;
  transform: translateY(-5px);
}

.wrap-btns {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 2;
}

.number {
  background-color: #dc080a;
  padding: 10px 15px;
  text-decoration: none;
  color: #fff;
  font-size: 25px;
  line-height: 28px;
  font-weight: 400;
  border-radius: 15px;
  transition: all 500ms ease;
}

@media (max-width: 1500px) {
  .desc,
  .number {
    font-size: 18px;
  }
}

@media (max-width: 930px) {
  .wrapper {
    padding: 90px 10px 20px 10px;
  }

  .wrapper2 {
    padding: 20px 10px;
  }
  .wrap-desc {
    width: 100%;
  }

  .desc {
    padding: 7px;
  }

  .group {
    width: 100%;
  }
}

@media (max-width: 700px) {
  img {
    width: 100%;
  }
  .desc,
  .number {
    font-size: 14px;
  }
}

@media (max-width: 500px) {
  img {
    width: 600px;
    height: 600px;
    object-fit: cover;
  }

  .wrapper {
    padding-top: 110px;
  }
}

@media (max-width: 420px) {
  .desc {
    padding: 4px 6px;
    font-size: 11px;
    text-align: center;
  }
}

@media (max-width: 350px) {
  .wrap-desc {
    flex-direction: column;
    gap: 10px;
  }
  .left,
  .right {
    align-items: stretch;
    justify-content: stretch;
    gap: 10px;
  }

  .desc {
    width: 160px;
    font-size: 13px;
    line-height: 10px;
    padding: 7px 10px;
  }
}
</style>
