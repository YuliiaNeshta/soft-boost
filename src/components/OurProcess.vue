<template>
  <div class="container">
    <div class="process">
      <h2 class="process__title title">
        А процесс?
      </h2>
      <div class="process__cards">
        <base-card-process
          title="Прототип"
          number="01"
					v-for="item in listItems"
					:key="item.title"
          :list="item"
        ></base-card-process>
        <base-card-process title="Исследование" number="02"></base-card-process>
      </div>
      <div class="process__cards process__cards--second-row">
        <base-card-process
          title="Создание дизайна"
          number="03"
        ></base-card-process>
        <base-card-process title="Отзывчивость" number="04"></base-card-process>
      </div>
    </div>
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
      listItems: [
        {
					title: 'Pfujkjd',
          item: "Раз",
          second: "Два",
          item2: "Три",
          item3: "Четыре",
        },
				{
					title: 'Pfujkjd333',
          item: "Раз",
          second: "Два",
          item2: "Три",
          item3: "Четыре",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.process {
  &__title {
    margin-bottom: 100px;
  }
  &__cards {
  }

  &__cards--second-row {
  }
}
</style>
