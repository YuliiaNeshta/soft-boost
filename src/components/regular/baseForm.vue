<template>
	<div class="form">
		<div class="form__row">
			<input class="form__input" type="text" placeholder="Имя">
			<input class="form__input" type="number" placeholder="Телефон">
		</div>
		<div class="form__row">
			<base-button>Общаться</base-button>
			<div class="form__social">
				<a class="form__link" href="#"><img src="@/assets/images/facebook.svg" alt="Our facebook" /></a>
				<a class="form__link" href="#"><img src="@/assets/images/linkedin.svg" alt="Our Linkedin" /></a>
				<a class="form__link"	href="#" ><img src="@/assets/images/instagram.svg" alt="Our Instagram" /></a>
			</div>
		</div>
		
	</div>
</template>

<script>
import baseButton from './baseButton'
export default {
  components: { baseButton },
}
</script>

<style lang="scss">
	.form {
		margin-top: 70px;

		&__row {
			display: flex;
		}
		&__link{
			display: flex;
		}

		&__input {
			-webkit-appearance: none;
			margin-bottom: 40px;
			margin-right: 30px;
			font-weight: 300;
			color: #fff;
			border: 0;
			background-color: transparent;
			border-bottom: 1px solid #FFFFFF;
			padding: 5px 0px;
			min-width: 240px;
			&::placeholder{
				font-weight: 300;
				color: #fff;
			}
			&:focus{
				outline: none;
			}
		}

		&__social {
			margin-left: 30px;
			display: flex;
			img{
				margin-right: 30px;
				cursor: pointer;
			}
		}
}

</style>