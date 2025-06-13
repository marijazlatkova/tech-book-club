<template>
  <HeroSection />
  <InfoSection />
  <Membership />
</template>

<script setup>
  import "./styles/fonts.css";
  import "./styles/global.css";
  import HeroSection from "./components/hero/HeroSection.vue";
  import InfoSection from "./components/info/InfoSection.vue";
  import Membership from "./components/membership/Membership.vue";
</script>