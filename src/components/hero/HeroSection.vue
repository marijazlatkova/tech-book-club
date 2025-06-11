<template>
  <section class="hero">
    <img :src="logo" class="logo" alt="Tech book club logo" />

    <div class="hero-left">
      <h1 class="hero-gradient">
        Join the ultimate tech book club
      </h1>

      <p class="description">
        Turn your reading time into learning time with fellow tech enthusiasts.
        Get curated recommendations, join vibrant discussions, and level up
        your skills one chapter at a time.
      </p>

      <button class="membership-btn">
        Review membership options
        <img :src="arrowIcon" alt="Arrow Icon" />
      </button>

      <div class="social-proof">
        <img :src="avatars" class="avatars" alt="Avatars" />

        <div class="stars-block">
          <div class="stars-row">
            <img v-for="n in 5" :key="n" :src="starIcon" alt="Star" />
          </div>
          <p class="developers">
            200+ developers joined already
          </p>
        </div>
      </div>
    </div>

    <img :src="heroImage" class="hero-image" alt="People reading" />
  </section>
</template>

<script setup>
  import logo from "@/assets/images/logo.svg";
  import arrowIcon from "@/assets/images/icon-arrow-down.svg";
  import avatars from "@/assets/images/image-avatars.webp";
  import starIcon from "@/assets/images/icon-star.svg";
  import heroImage from "@/assets/images/image-hero-mobile.webp";
</script>

<style scoped>
  .hero {
    background-color: rgb(250, 245, 243);
    background-image: url("@/assets/images/pattern-light-bg.svg"), url("@/assets/images/pattern-glow.svg");
    background-position: top left, top right;
    background-size: cover;
    background-repeat: no-repeat;
    padding: 40px 20px;
    display: grid;
    grid-template-columns: 1fr;
    align-items: center;
    gap: 20px;
    overflow-x: hidden;
    position: relative;
  }

  .logo {
    width: 200px;
    height: auto;
    padding-bottom: 20px;
  }

  .hero-gradient {
    width: 100%;
    background: linear-gradient(107deg, rgb(255, 154, 96) -8%, rgb(6, 38, 48) 60%);
    background-clip: text;
    color: transparent;
    font-family: "Martian Mono", monospace;
    font-size: 30px;
    font-weight: 700;
    line-height: 40px;
    padding-bottom: 30px;
    margin: 0;
  }

  .description {
    color: rgb(56, 81, 89);
    padding-bottom: 30px;
    font-size: 20px;
    margin: 0;
  }

  .membership-btn {
    font-family: "Martian Mono", monospace;
    font-size: 16px;
    font-weight: 600;
    letter-spacing: -0.33px;
    text-transform: uppercase;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 16px;
    padding: 16px 0;
    border: 2px solid rgb(31, 31, 31);
    border-radius: 8px;
    background: rgb(255, 245, 239);
    color: rgb(31, 31, 31);
    margin-bottom: 30px;
  }

  .social-proof {
    display: flex;
    align-items: center;
    gap: 16px;
    margin: 20px 0;
  }

  .avatars {
    width: 160px;
    height: auto;
  }

  .stars-block {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .stars-row {
    display: flex;
  }

  .developers {
    font-family: "Martian Mono", monospace;
    margin: 0;
    font-size: 12px;
    color: rgb(68, 68, 68);
    letter-spacing: -0.33px;
  }

  .hero-image {
    width: 100%;
    border-radius: 25px;
    object-fit: cover;
  }

  @media (min-width: 768px) {
    .hero {
      padding: 40px;
    }

    .hero-gradient {
      font-size: 42px;
      line-height: 48px;
    }

    .description {
      font-size: 20px;
    }

    .membership-btn {
      font-size: 17px;
    }
  }

  @media (min-width: 1440px) {
    .hero {
      padding: 40px 180px;
      grid-template-columns: 1fr 1fr;
      align-items: center;
      gap: 40px;
    }

    .logo {
      position: absolute;
      top: 50px;
      left: 180px;
      z-index: 10;
      padding-bottom: 0;
    }

    .hero-left {
      display: flex;
      flex-direction: column;
      gap: 20px;
      padding-top: 80px;
    }

    .hero-gradient {
      font-size: 54px;
      line-height: 70px;
      padding-bottom: 10px;
    }

    .description {
      font-size: 22px;
      padding-bottom: 13px;
    }

    .membership-btn {
      width: 80%;
      font-size: 18px;
      padding: 18px;
      margin: 0;
    }

    .social-proof {
      margin: 10px 0;
    }

    .developers {
      font-size: 14px;
    }
  }
</style>