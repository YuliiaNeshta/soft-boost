<template>
  <div class="home-wrap">
    <div class="container">
      <div class="home">
        <div class="home__logo">
          <img src="@/assets/images/logo.svg" alt="Soft Boost" />
          <div class="spot-yellow"></div>
        </div>
        <div class="home__info">
          <h1 class="home__title">
            Цифровое сердце<br /><span>вашего бизнеса</span>
          </h1>
          <p class="home__text">
            Качественно разработаем приложения на современных платформах и
            запустим его вместе.
          </p>
          <base-button>Хочу сотрудничать!</base-button>
        </div>
      </div>
    </div>
    <div class="marquee">
      <ul class="marquee-content marquee-help">
        <li>Design</li>
        <li>Development</li>
        <li>Testing</li>
        <li>Management</li>
        <li>Analytics</li>
        <li>Design</li>
        <li>Development</li>
        <li>Testing</li>
        <li>Management</li>
        <li>Analytics</li>
        <li>Design</li>
        <li>Development</li>
        <li>Testing</li>
        <li>Management</li>
        <li>Analytics</li>
      </ul>
    </div>
  </div>
</template>

<script>
import baseButton from "./regular/baseButton";

export default {
  components: { baseButton },
  mounted() {
    const root = document.documentElement;
    const marqueeElemDisplayed = getComputedStyle(root).getPropertyValue(
      "--marquee-elem-displayed"
    );
    const marqueeContent = document.querySelector(".marquee-content");

    root.style.setProperty("--marquee-elem", marqueeContent.children.length);
    marqueeContent.style.padding = "0px 50px";
    for (let i = 0; i < marqueeElemDisplayed; i++) {
      marqueeContent.appendChild(marqueeContent.children[i].cloneNode(true));
    }
  },
};
</script>

<style lang="scss">
.home-wrap .container {
  margin-bottom: 106px;
}

.home {
  display: flex;
  padding-top: 226px;
  margin-bottom: 60px;
  &-wrap {
    margin: 0px -50px;
  }

  &__logo {
    width: 50%;
    position: relative;
  }

  &__text {
    margin-bottom: 22px;
    max-width: 505px;
  }

  &__title {
    font-size: 60px;
    line-height: 72px;
    color: $blue;
    margin-bottom: 20px;
    span {
      color: $yellow;
    }
  }
}

:root {
  --marquee-width: 100%;
  --marquee-height: 100px;
  --marquee-elem-displayed: 5;
  --marquee-elem-width: calc(
    var(--marquee-width) / var(--marquee-elem-displayed)
  );
}

.marquee {
  max-width: 100%;
  width: var(--marquee-width);
  height: var(--marquee-height);
  background-color: $blue;
  color: #fff;
  overflow: hidden;
  transform: rotate(4deg);
  margin-top: 60px;
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
}
.marquee-content {
  height: 100%;
  display: flex;
  animation: scrolling 25s linear infinite;
  & li {
    display: flex;
    justify-content: center;
    align-items: center;
    width: var(--marquee-elem-width);
    // flex-shrink: 0;
    flex: 1 1 auto;
    margin-right: 35px;
    font-size: 45px;
    white-space: nowrap;
  }
}

.marquee-help {
  display: flex;
}
@keyframes scrolling {
  0% {
    transform: translateX(0vw);
  }
  100% {
    transform: translateX(
      calc(-1 * var(--marquee-elem-width) * var(--marquee-elem))
    );
  }
}
</style>
