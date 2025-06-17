<template>
  <HeroSection />
  <InfoSection />
  <Membership />
  <Footer />
</template>

<script setup>
  import "./styles/fonts.css";
  import "./styles/global.css";
  import HeroSection from "./components/Hero/HeroSection.vue";
  import InfoSection from "./components/Info/InfoSection.vue";
  import Membership from "./components/Membership/Membership.vue";
  import Footer from "./components/Footer/Footer.vue";
</script>