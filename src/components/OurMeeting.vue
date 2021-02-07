<template>
  <div class="container">
    <div class="meeting">
      <div class="meeting__column">
        <h2 class="meeting__title title">
          Давайте знакомиться
        </h2>
        <img src="@/assets/images/arrow.svg" alt="" />
      </div>
      <div class="meeting__column">
        <p class="meeting__text">
          <strong>Мы - команда прогрессивных мечтателей</strong>, которые
          вдохновляются современными стартапами и технологиями на рынке IT. Мы
          интегрируем прогрессивные технологии в существующие бизнесы, создаем
          некий диджитализированый бустер и апгрейд, который утоляет бизнес
          потребность нашего клиента, а в последствии и его клиентов. Совместно
          с командой разрабатываем инновационное для компаний решение переводя
          существующие оффлайн процессы в онлайн. Так же помогаем стартапам в
          реализации задуманной идеи.
        </p>
        <strong>Нашими особенностями являются:</strong>
        <ol class="meeting__list">
          <li>1. Френдли коммуникация с заказчиком</li>
          <li>2. Полное выявление потребности</li>
          <li>3. Завершаем проект только при 100% удовлетворении заказчика</li>
          <li>4. Заводим отношения не на единоразовой основе, а на долгие-долгие периоды сотрудничества</li>
        </ol>
        <p class="meeting__line">Так все же кто мы?</p>
        <strong>Мы - твой турбо-ускоритель в диджитализации.</strong>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">

.meeting {
	padding: 200px 0px;
	display: flex;

		&__column {
			width: 50%;
			img{
				margin-top: 40px;
			}
		}

		&__title {
			font-size: 60px;
			line-height: 72px;
		}

		&__text {
			margin-bottom: 25px;
			letter-spacing: 0.015em;
		}

		&__list {
		}

		&__line {
		}
}

</style>
