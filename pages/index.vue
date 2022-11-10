<template>
  <div class="home">
    <app-home-intro></app-home-intro>
    <app-home-features></app-home-features>
    <app-home-banner></app-home-banner>
    <app-home-experience></app-home-experience>
    <app-home-banner-2></app-home-banner-2>
    <app-home-why></app-home-why>
  </div>
</template>

<script>
import AppHomeFeatures from '../components/home/AppHomeFeatures.vue'
import AppHomeIntro from '../components/home/AppHomeIntro.vue'
import AppHomeBanner from '../components/home/AppHomeBanner.vue'
import AppHomeExperience from '../components/home/AppHomeExperience.vue'
import AppHomeBanner2 from '../components/home/AppHomeBanner2.vue'
import AppHomeWhy from '../components/home/AppHomeWhy.vue'

export default {
  name: 'Home',
  components: {
    AppHomeIntro,
    AppHomeFeatures,
    AppHomeBanner,
    AppHomeExperience,
    AppHomeBanner2,
    AppHomeWhy
  }
}
</script>
