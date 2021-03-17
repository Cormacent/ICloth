<template>
  <div class="home">
    <header-section />
    <hero-section />
    <banner-section />
    <insta-section />
    <partner-section />
    <footer-section />
  </div>
</template>

<script>
import HeaderSection from "@/components/HeaderSection.vue";
import HeroSection from "@/components/HeroSection.vue";
import BannerSection from "@/components/BannerSection.vue";
import InstaSection from "@/components/InstaSection.vue";
import PartnerSection from "@/components/PartnerSection.vue";
import FooterSection from "../components/FooterSection.vue";

export default {
  name: "Home",
  components: {
    HeaderSection,
    HeroSection,
    BannerSection,
    InstaSection,
    PartnerSection,
    FooterSection,
  },
};
</script>

<style scoped>
</style>