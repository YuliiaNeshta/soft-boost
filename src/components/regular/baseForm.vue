<template>
  <form class="form" @submit.prevent="onSubmit">
    <div class="form__row">
      <input
        class="form__input"
        type="text"
        :placeholder="$t('formPlaceholderName')"
        v-model="name"
      />
      <input
        class="form__input"
        type="number"
        :placeholder="$t('formPlaceholderMobile')"
        v-model="mobile"
      />
    </div>
    <div class="form__row">
      <button class="form__btn" type="submit">
        <slot>
          {{ title }}
        </slot>
      </button>
      <div class="form__social">
        <a class="form__link" href="#"
          ><img src="@/assets/images/facebook.svg" alt="Our facebook"
        /></a>
        <a class="form__link" href="#"
          ><img src="@/assets/images/linkedin.svg" alt="Our Linkedin"
        /></a>
        <a class="form__link" href="#"
          ><img src="@/assets/images/instagram.svg" alt="Our Instagram"
        /></a>
      </div>
    </div>
  </form>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      mobile: "",
    };
  },
  props: {
    title: String,
  },
  methods: {
    onSubmit() {
      const formData = {
        name: this.name,
        mobile: this.mobile,
      };
      console.log(formData);
    },
  },
};
</script>

<style lang="scss">
.form {
  &__row {
    display: flex;
    @include for-tablet {
      flex-direction: column;
      & .button-wrap {
        margin-bottom: 25px;
      }
    }
  }
  &__link {
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
    border-bottom: 1px solid #ffffff;
    padding: 5px 0px;
    min-width: 240px;
    font-size: 16px;
    line-height: 20px;
    @include for-tablet {
      max-width: 220px;
      width: 100%;
    }
    &::placeholder {
      font-weight: 300;
      color: #fff;
      font-size: 16px;
      line-height: 20px;
    }
    &:focus {
      outline: none;
    }
  }

  &__social {
    margin-left: 30px;
    display: flex;
    @include for-tablet {
      margin-left: 0px;
    }
    img {
      margin-right: 30px;
      cursor: pointer;
    }
  }
  &__btn {
    background-color: $yellow;
    font-size: 16px;
    line-height: 19px;
    padding: 16px 42px;
    max-width: 240px;
    transition: all 0.3s ease 0s;
		@include for-tablet{
			margin-bottom: 25px;
		}
    
    &:hover {
      filter: drop-shadow(0px 4px 20px rgba(255, 255, 255, 0.15));
      background-color: #fadc1b;
    }
  }
}
</style>
