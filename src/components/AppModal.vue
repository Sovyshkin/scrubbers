<script>
export default {
  name: "AppModal",
  components: {},
  data() {
    return {
      message: "",
    };
  },
  methods: {
    close() {
      try {
        this.$emit("close");
      } catch (err) {
        console.log(err);
      }
    },
    async copyText() {
      try {
        await navigator.clipboard.writeText("+7 (3532) 30-77-17");
        this.message = "Скопировано";
        setTimeout(() => {
          this.message = "";
        }, 1000);
      } catch (err) {
        console.error("Ошибка при копировании:", err);
      }
    },
  },
  mounted() {},
};
</script>
<template>
  <div class="card">
    <div class="cancel">
      <span class="title">Запрос стоимости</span>
      <img @click="close" src="../assets/close.png" alt="" />
    </div>
    <div class="group" @click="copyText">
      <img class="phone" src="../assets/phone.png" alt="" />
      <span>+7 (3532) 30-77-17</span>
      <img class="copy" src="../assets/copy.png" alt="" />
    </div>
    <a class="call" href="tel: +7 (3532) 30-77-17" v-if="!message">Позвонить</a>
    <div class="msg success" v-if="message">{{ message }}</div>
  </div>
</template>
<style scoped>
.card {
  position: relative;
  display: flex;
  flex-direction: column;
  gap: 25px;
  padding: 32px;
  border-radius: 20px;
  background-color: #1c263f;
  min-width: 350px;
}
.title {
  font-size: 24px;
  line-height: 26px;
  font-weight: 600;
  color: #fff;
}
.cancel {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.cancel img {
  cursor: pointer;
  height: 24px;
  width: 24px;
}

.group {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 15px;
}

.phone {
  width: 32px;
  height: 32px;
}

.group span {
  font-weight: 600;
  font-size: 19px;
  line-height: 19px;
  color: #fff;
}

.copy {
  height: 24px;
  width: 24px;
}

.call {
  width: 100%;
  padding: 12px;
  background: linear-gradient(90deg, #feb803 0%, #ff9a06 100%);
  border-radius: 15px;
  color: #030a1c;
  font-weight: 500;
  font-size: 22px;
  line-height: 25px;
  transition: all 500ms ease;
  text-align: center;
}

.msg {
  padding: 10px 13px;
  font-size: 16px;
  color: #030a1c;
  line-height: 16px;
  border-radius: 15px;
  width: fit-content;
  margin: 0 auto;
}

.success {
  background-color: #ff9a06;
}
</style>
