<template>
  <div class="home-wrap" id="home">
    <base-modal v-if="isFormPopupVisible" @closePopup="closePopup"></base-modal>
    <div class="container">
      <div class="home">
        <div class="home__logo">
          <img src="@/assets/images/logo.svg" alt="Soft Boost" />
					<!-- <video class="home__logo--video" src="@/assets/images/logo-video.mov"></video> -->
          <div class="spot-yellow"></div>
        </div>
        <div class="home__info">
          <h1 class="home__title">
            {{ $t("mainTitle_1")}} <br /><span>{{ $t("mainTitle_2")}}</span>
          </h1>
          <p class="home__text">
            {{ $t("mainText")}}
          </p>
          <base-button @showModal="showModal">{{ $t("btnHome")}}</base-button>
        </div>
      </div>
    </div>
    <marquee-text :repeat="10">
      <p>Design</p>
      <p>Development</p>
      <p>Testing</p>
      <p>Management</p>
      <p>Analytics</p>
    </marquee-text>
  </div>
</template>

<script>
import baseButton from "./regular/baseButton";
import BaseModal from "./regular/baseModal";
import MarqueeText from "vue-marquee-text-component";

export default {
  components: { baseButton, BaseModal, MarqueeText },
  data() {
    return {
      isFormPopupVisible: false,
    };
  },

  methods: {
    showModal() {
      this.isFormPopupVisible = true;
    },
    closePopup() {
      this.isFormPopupVisible = false;
    },
    
  },
};
</script>

<style lang="scss">
.home-wrap .container {
  margin-bottom: 106px;
}
.marquee-text-wrap {
  max-width: 100%;
  width: 110vw;
  padding: 25px 0px;
  background-color: $blue;
  overflow: hidden;
  transform: rotate(4deg);
  margin-top: 60px;
}

.marquee-text-text {
  display: flex;
  p {
    margin-right: 26px;
    font-family: "Zilla Slab", serif;
    font-weight: 700;
    font-size: 40px;
    line-height: 48px;
    color: #fff;
    white-space: nowrap;
  }
}

.home {
  display: flex;
  padding-top: 226px;
  margin-bottom: 60px;
  @include for-tablet {
    flex-direction: column;
    padding-top: 150px;
  }
  @include for-min-desctop {
    padding: 0px 50px;
    padding-top: 150px;
  }
  &-wrap {
    margin: 0px -50px;
    @include for-tablet {
      margin: 0px -30px;
    }
  }

  &__logo {
    width: 50%;
    position: relative;

    @include for-tablet {
      img {
        width: 100%;
        height: 175px;
      }
      margin-bottom: 76px;
      width: 100%;
    }
  }

  &__text {
    margin-bottom: 22px;
    max-width: 505px;
    @include for-tablet {
      margin-bottom: 30px;
    }
  }
  &__info {
    @include for-min-desctop {
      flex: 1 1 50%;
      margin-left: 20px;
    }
  }

  &__title {
    font-size: 60px;
    line-height: 72px;
    color: $blue;
    margin-bottom: 20px;
    @include for-min-desctop {
      font-size: 45px;
      line-height: 55px;

      br {
        display: none;
      }
    }
    @include for-mobile {
      font-size: 30px;
      line-height: 37px;
    }
    span {
      color: $yellow;
    }
  }
}

.spot-yellow {
  width: 70px;
  height: 70px;
  position: absolute;
  right: 11%;
  bottom: -124px;
  background-color: $yellow;
  filter: blur(40px);
  opacity: 0.7;
  @include for-mobile {
    display: none;
  }
}
</style>
