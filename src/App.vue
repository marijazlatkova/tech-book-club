<template>
  <HeroSection />
  <InfoSection />
  <Membership />
  <Footer />
</template>

<script setup>
  import "./styles/fonts.css";
  import "./styles/global.css";
  import HeroSection from "./components/hero/HeroSection.vue";
  import InfoSection from "./components/info/InfoSection.vue";
  import Membership from "./components/membership/Membership.vue";
  import Footer from "./components/footer/Footer.vue";
</script>