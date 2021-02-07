<template>
  <div class="card">
    <div class="card__number">{{ number }}</div>
    <p class="card__title">{{ title }}</p>
    <ul class="card__list">
        <slot></slot>
    </ul>
  </div>
</template>

<script>
//card-number пропса
//card list разное колво li
//card title
export default {
	data() {
    return {
			items: [
				{ message: '— Брифинг' },
      	{ message: '— Общение с заказчиком' }
			]
		}
  },
  props: {
    title: {
      type: String,
      default: "Процесс",
    },
    number: {
      type: String,
      default: "01",
    },
		list: {
			type: Object,
			default(){
				return {}
			}
		}
  },
};
</script>

<style lang="scss">
.card {
  flex: 0 1 420px;
  border: 1px solid $blue;
  position: relative;
  padding: 30px 70px 20px 40px;
  margin-bottom: 30px;
  margin-right: 30px;

  &__number {
    position: absolute;
    right: 35px;
    top: 27px;
    width: 35px;
    height: 35px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: $yellow;
    border: 1px solid $blue;
    border-radius: 50%;
  }

  &__title {
    font-size: 24px;
    line-height: 29px;
    font-weight: 700;
    margin-bottom: 20px;
  }

  &__list {
  }
}
</style>
