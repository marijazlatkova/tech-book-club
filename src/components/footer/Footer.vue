<template>
  <footer class="footer">
    <h2 class="footer-title">Ready to debug your reading list?</h2>

    <button class="footer-btn">
      Review membership options
      <img :src="arrowIcon" alt="Arrow Icon" />
    </button>

    <div class="footer-social">
      <img :src="avatars" class="avatars" alt="Avatars" />

      <div class="stars-block">
        <div class="stars-row">
          <img v-for="n in 5" :key="n" :src="starIcon" alt="Star" />
        </div>

        <p class="developers">200+ developers joined already</p>
      </div>
    </div>

    <div class="footer-bottom">
      <p class="copyright">© 2025 - Tech Book Club</p>

      <div class="logos">
        <img :src="blueskyLogo" alt="Bluesky logo" />
        <img :src="linkedinLogo" alt="LinkedIn logo" />
      </div>
    </div>
  </footer>
</template>

<script setup>
  import arrowIcon from "@/assets/images/icon-arrow-up.svg";
  import avatars from "@/assets/images/image-avatars.webp";
  import starIcon from "@/assets/images/icon-star.svg";
  import blueskyLogo from "@/assets/images/logo-bluesky.svg";
  import linkedinLogo from "@/assets/images/logo-linkedin.svg";
</script>

<style scoped>
  .footer {
    background: rgb(6, 38, 48) url("@/assets/images/pattern-dark-bg.svg");
    color: rgb(250, 245, 243);
    border-top-left-radius: 20px;
    border-top-right-radius: 20px;
    padding: 50px 20px 20px 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 32px;
  }

  .footer-title {
    font-family: "Martian Mono", monospace;
    font-size: 26px;
    font-weight: 700;
    text-align: center;
    line-height: 36px;
    margin: 0;
  }

  .footer-btn {
    font-family: "Martian Mono", monospace;
    font-size: 16px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: -0.3px;
    background: transparent;
    color: rgb(255, 255, 255);
    border: 2px solid rgb(255, 255, 255);
    border-radius: 8px;
    padding: 16px 20px;
    display: flex;
    align-items: center;
    gap: 12px;
    cursor: pointer;
  }

  .footer-social {
    display: flex;
    align-items: center;
    gap: 16px;
  }

  .avatars {
    width: 120px;
    height: auto;
  }

  .stars-row {
    display: flex;
    gap: 4px;
  }

  .developers {
    font-family: "Martian Mono", monospace;
    font-size: 14px;
    color: rgb(250, 245, 243);
    margin: 4px 0 0;
  }

  .footer-bottom {
    font-family: "Martian Mono", monospace;
    font-size: 14px;
    color: rgb(250, 245, 243);
    border-top: 1px solid rgb(56, 81, 89);
    width: 100%;
    padding-top: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 5px;
  }

  .logos {
    display: flex;
    gap: 20px;
  }

  @media (min-width: 768px) {
    .footer {
      position: relative;
      padding: 60px 40px 20px 40px;
      gap: 40px;
    }

    .footer-title {
      font-size: 34px;
      line-height: 56px;
    }

    .footer-btn {
      padding: 18px 24px;
    }

    .avatars {
      width: 140px;
    }

    .footer-bottom {
      padding-top: 20px;
      border-top: none;
      position: relative;
      flex-direction: row;
      justify-content: space-between;
    }

    .footer-bottom::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      transform: translateX(-40px);
      width: calc(100% + 80px);
      height: 1px;
      background-color: rgb(56, 81, 89);
    }
  }

  @media (min-width: 1440px) {
    .footer {
      padding: 60px 180px 26px 180px;
      gap: 60px;
    }

    .footer-title {
      font-size: 42px;
    }

    .footer-btn {
      font-size: 18px;
      padding: 20px 28px;
    }

    .avatars {
      width: 160px;
    }

    .footer-bottom {
      padding-top: 26.5px;
    }
  }
</style>