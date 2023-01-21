<template>
  <div class="home">
    <app-home-intro :slides="slides"></app-home-intro>
    <app-home-partners :partners="partners" />
    <app-home-features :services="services"></app-home-features>
    <app-home-banner :topBanner="topBanner"></app-home-banner>
    <app-home-experience></app-home-experience>
    <app-home-banner-2></app-home-banner-2>
    <app-home-activities :activities="activities" />
    <app-home-steps :steps="steps" />
    <app-home-why :teams="teams"></app-home-why>
  </div>
</template>

<script>
import AppHomeFeatures from "../components/home/AppHomeFeatures.vue";
import AppHomeIntro from "../components/home/AppHomeIntro.vue";
import AppHomeBanner from "../components/home/AppHomeBanner.vue";
import AppHomeExperience from "../components/home/AppHomeExperience.vue";
import AppHomeBanner2 from "../components/home/AppHomeBanner2.vue";
import AppHomeWhy from "../components/home/AppHomeWhy.vue";
import AppHomeActivities from "../components/home/AppHomeActivities.vue";
import AppHomeSteps from "../components/home/AppHomeSteps.vue";
import AppHomePartners from "../components/home/AppHomePartners.vue";

export default {
  name: "Home",
  components: {
    AppHomeIntro,
    AppHomeFeatures,
    AppHomeBanner,
    AppHomeExperience,
    AppHomeBanner2,
    AppHomeWhy,
    AppHomeActivities,
    AppHomeSteps,
    AppHomePartners,
  },
  async asyncData({ $axios, app }) {
    const slides = await $axios.get("/sliders", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const partners = await $axios.get("/partners");

    const services = await $axios.get("/services");

    const topBanner = await $axios.get("/sections/banner-top", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const teams = await $axios.get("/teams");

    const activities = await $axios.get("/sections/activities", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const steps = await $axios.get("/sections/steps", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    return {
      slides: slides.data.data.sliders,
      partners: partners.data.data.partners,
      services: services.data.data.services,
      topBanner: topBanner.data.data,
      teams: teams.data.data.teams,
      activities: activities.data.data,
      steps: steps.data.data,
    };
  },
};
</script>
