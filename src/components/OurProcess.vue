<template>
  <div class="container">
    <div class="process">
      <h2 class="process__title title">
        А процесс?
      </h2>
      <div class="process__cards">
        <base-card-process title="Прототип" number="01">
          <li
            class="process__item"
            v-for="itemLi in listItems.prototype"
            :key="itemLi"
          >
            — {{ itemLi }}
          </li>
        </base-card-process>
        <base-card-process title="Исследование" number="02">
          <li
            class="process__item"
            v-for="itemLi in listItems.study"
            :key="itemLi"
          >
            — {{ itemLi }}
          </li>
        </base-card-process>
      </div>
      <div class="process__cards process__cards--second-row">
        <base-card-process title="Создание дизайна" number="03">
          <li
            class="process__item"
            v-for="itemLi in listItems.design"
            :key="itemLi"
          >
            — {{ itemLi }}
          </li>
        </base-card-process>
        <base-card-process title="Отзывчивость" number="04">
          <li
            class="process__item"
            v-for="itemLi in listItems.responsiveness"
            :key="itemLi"
          >
            — {{ itemLi }}
          </li>
        </base-card-process>
      </div>
      <div class="light-pink-spot"></div>
    </div>
    <h3 class="process__quote">
      Никаких общих фраз, пустых обещаний и равнодушного отношения
    </h3>
  </div>
</template>

<script>
import baseCardProcess from "./regular/baseCardProcess";

export default {
  //у вас в объекте в объявлении props нету listItems
  //А ещё тут же на стрелочке cardItem неизвестная переменная.
  components: { baseCardProcess },
  data() {
    return {
      listItems: {
        prototype: ["Брифинг", "Общение с заказчиком", "Прототипирование"],
        study: ["Поиск референсов", "Брейншторм", "Концепт"],
        design: [
          "Подбор шрифтов",
          "Подбор цветовой палитры",
          "Создание креативного UI",
        ],
        responsiveness: ["Версия для планшета", "Мобильная версия"],
      },
    };
  },
};
</script>

<style lang="scss">
.process {
  position: relative;
  &__title {
    margin-bottom: 100px;
  }
  &__cards {
    display: flex;
    flex-wrap: wrap;
  }
  &__item {
    margin-bottom: 10px;
    font-weight: 300;
    letter-spacing: 0.015em;
  }
  &__cards--second-row {
    justify-content: center;
    margin-left: 150px;
    position: relative;
    z-index: 2;
  }
  &__quote {
    margin: 200px 0px;
    text-align: center;
    font-weight: 700;
    font-size: 40px;
    line-height: 49px;
    text-align: center;
  }
}

.light-pink-spot {
  position: absolute;
  right: -120px;
  bottom: -100px;
  width: 261px;
  height: 261px;
  background: #edd6ff;
  filter: blur(60px);
  opacity: 0.7;
}
</style>
