<template>
  <div class="home">
    <app-home-intro :slides="slides"></app-home-intro>
    <app-home-partners :partners="partners" />
    <app-home-features :services="services"></app-home-features>
    <div v-if="$store.state.sectionsStatus['banner-top']">
      <app-home-banner :topBanner="topBanner.data"></app-home-banner>
    </div>
    <app-home-experience></app-home-experience>
    <app-home-banner-2></app-home-banner-2>
    <div v-if="$store.state.sectionsStatus.activities">
      <app-home-activities :activities="activities.data" />
    </div>
    <div v-if="$store.state.sectionsStatus.steps">
      <app-home-steps :steps="steps.data" />
    </div>
    <app-home-why :teams="teams"></app-home-why>
    <SocialChat :attendants="attendants">
      <p slot="header">Click one of our representatives below to chat.</p>
      <template v-slot:button="{ open }">
        <span v-show="!open">Contact us</span>
        <span v-show="open">Close</span>
      </template>
      <small slot="footer">Opening hours: 8am to 10pm</small>
    </SocialChat>
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
  data() {
    return {
      attendants: [
        {
          app: "whatsapp",
          label: "Support",

          name: this.$store.state.websiteSettings.find(
            (one) => one.key === "chat_widget_whatsapp_label"
          )
            ? this.$store.state.websiteSettings.find(
                (one) => one.key === "chat_widget_whatsapp_label"
              ).plain_value
            : "Laravada",

          number: this.$store.state.websiteSettings.find(
            (one) => one.key === "chat_widget_whatsapp_number"
          )
            ? this.$store.state.websiteSettings.find(
                (one) => one.key === "chat_widget_whatsapp_number"
              ).plain_value
            : "11111111111",

          avatar: {
            src: "https://avatars0.githubusercontent.com/u/8084606?s=460&u=20b6499a416cf7129a18e5c168cf387e159edb1a&v=4",
            alt: "Laravada customer support",
          },
        },
        {
          app: "messenger",
          label: "Technical support",

          name: this.$store.state.websiteSettings.find(
            (one) => one.key === "chat_widget_messenger_label"
          )
            ? this.$store.state.websiteSettings.find(
                (one) => one.key === "chat_widget_messenger_label"
              ).plain_value
            : "Laravada Facebook",

          id: this.$store.state.websiteSettings.find(
            (one) => one.key === "chat_widget_messenger_id"
          )
            ? this.$store.state.websiteSettings.find(
                (one) => one.key === "chat_widget_messenger_id"
              ).plain_value
            : "111111111111",

          avatar: {
            src: "https://avatars0.githubusercontent.com/u/8084606?s=460&u=20b6499a416cf7129a18e5c168cf387e159edb1a&v=4",
            alt: "Laravada customer support",
          },
        },
      ],
    };
  },
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
      topBanner: topBanner.data,
      teams: teams.data.data.teams,
      activities: activities.data,
      steps: steps.data,
    };
  },
};
</script>

<style>
.home {
  --vsc-bg-header: var(--main-color);
  --vsc-bg-footer: var(--main-color);
  --vsc-text-color-header: #000;
  --vsc-text-color-footer: #000;
  --vsc-bg-button: var(--main-color);
  --vsc-text-color-button: #000;
  --vsc-outline-color: var(--main-color);
  --vsc-border-color-bottom-header: #fff;
  --vsc-border-color-top-footer: #fff;
}
</style>
