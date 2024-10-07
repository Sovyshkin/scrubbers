<script>
/* eslint-disable */
export default {
  data() {
    return {};
  },
  methods: {
    async renderMap() {
      ymaps.ready(init); // когда апи готово, инициализируемя карту
      var customMap; // объявим переменную для карты
      async function init() {
        // функция инициализации
        customMap = new ymaps.Map("customMap", {
          // создадим карту выведем ее в див с id="customMap"
          center: [51.802146, 55.155211], // центра карты
          behaviors: ["default", "scrollZoom"], // скроллинг колесом
          zoom: 17, // масштаб карты
          controls: ["zoomControl", "fullscreenControl"], // элементы управления
        });

        customMap.controls.remove("geolocationControl"); // удаляем геолокацию
        customMap.controls.remove("searchControl"); // удаляем поиск
        customMap.controls.remove("trafficControl"); // удаляем контроль трафика
        customMap.controls.remove("typeSelector"); // удаляем тип
        customMap.controls.remove("fullscreenControl"); // удаляем кнопку перехода в полноэкранный режим
        customMap.controls.remove("zoomControl"); // удаляем контрол зуммирования
        customMap.controls.remove("rulerControl"); // удаляем контрол правил
        const placemark = new ymaps.Placemark(
          [51.802146, 55.155211],
          {},
          {
            iconLayout: "default#image",
            iconImageHref: "../assets/metka.png", // путь к стандартному изображению
            iconImageSize: [32, 32],
            iconImageOffset: [-16, -16],
          }
        );

        customMap.geoObjects.add(placemark);
      }
    },
  },
  mounted() {
    this.renderMap();
  },
};
</script>

<template>
  <div id="customMap" class="map"></div>
</template>

<style scoped>
.map {
  width: 100%;
  height: 30vh;
}
</style>
