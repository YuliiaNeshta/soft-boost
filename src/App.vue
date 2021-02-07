<template>
  <div class="wrapper">
		<base-header/>
		<home-page/>
		<our-meeting/>
		<our-process/>
  </div>
</template>

<script>
import HomePage from './components/HomePage';
import OurMeeting from './components/OurMeeting';
import OurProcess from './components/OurProcess';
import baseHeader from './components/regular/baseHeader';

export default {
  components: { baseHeader, HomePage, OurMeeting, OurProcess },
  name: "App",
};
</script>

<style lang="scss">
	.wrapper{
		overflow: hidden;
		color: red;
	}
</style>
