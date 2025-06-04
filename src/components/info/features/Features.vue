<template>
  <section class="features">
    <div class="features-block reverse">
      <div class="features-text">
        <h2 class="features-title">Read together, grow together</h2>
        <ul class="features-list">
          <li v-for="(item, index) in features" :key="index" class="features-item">
            <img :src="checkIcon" class="check-icon" alt="Check icon" />
            {{ item }}
          </li>
        </ul>
      </div>

      <img :src="readTogetherImage" class="features-image" alt="People reading together" />
    </div>

    <div class="features-block">
      <div class="features-text">
        <h2 class="features-title">
          Not your average book <span class="circle-highlight">club</span>
        </h2>

        <p class="features-description">
          Connect with a community that speaks your language - from
          <span class="highlight">Python</span> to
          <span class="highlight">TypeScript</span> and everything in between.
          Our discussions blend technical depth with practical applications.
        </p>
      </div>

      <div class="image-wrapper">
        <img :src="notAverageImage" class="features-image" alt="People discussing tech books" />

        <div class="features-icon">
          <img :src="logoTech" class="tech-logo" alt="Tech logo" />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
  import readTogetherImage from "@/assets/images/image-read-together-mobile.webp";
  import notAverageImage from "@/assets/images/image-not-average-mobile.webp";
  import checkIcon from "@/assets/images/icon-check.svg";
  import logoTech from "@/assets/images/logos-tech.svg";

  const features = [
    "Monthly curated tech reads selected by industry experts",
    "Virtual and in-person meetups for deep-dive discussions",
    "Early access to new tech book releases",
    "Author Q&A sessions with tech thought leaders",
  ];
</script>

<style scoped>
  .features {
    padding: 50px 20px;
    display: flex;
    flex-direction: column;
    gap: 30px;
  }

  .features-block {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  .features-text {
    display: flex;
    flex-direction: column;
    gap: 25px;
    padding: 25px 0;
  }

  .features-title {
    font-family: "Martian Mono", monospace;
    font-size: 26px;
    line-height: 34px;
    margin: 0;
  }

  .features-list {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    flex-direction: column;
    gap: 12px;
  }

  .features-item {
    display: flex;
    align-items: center;
    gap: 12px;
    line-height: 1.5;
    color: rgb(56, 81, 89);
    font-size: 20px;
  }

  .check-icon {
    width: 16px;
    height: 16px;
  }

  .features-image {
    width: 100%;
    border-radius: 25px;
    object-fit: cover;
  }

  .circle-highlight {
    position: relative;
    display: inline-block;
    z-index: 0;
  }

  .circle-highlight::after {
    content: "";
    position: absolute;
    left: -6px;
    top: -6px;
    width: 130%;
    height: 130%;
    border: 2px solid rgb(242, 126, 69);
    border-radius: 50%;
    z-index: -1;
    transform: rotate(-5deg);
    pointer-events: none;
  }

  .features-description {
    color: rgb(56, 81, 89);
    font-size: 20px;
    line-height: 1.5;
    margin: 0;
  }

  .highlight {
    font-weight: 600;
  }

  .features-icon {
    display: none;
  }

  @media screen and (min-width: 768px) {
    .features {
      padding: 40px;
    }

    .features-title {
      font-size: 32px;
      line-height: 40px;
    }

    .image-wrapper {
      position: relative;
    }

    .features-icon {
      position: absolute;
      bottom: 16px;
      right: 16px;
      display: block;
    }

    .tech-logo {
      width: 100px;
      height: auto;
    }
  }

  @media screen and (min-width: 1280px) {
    .features {
      padding: 60px 80px;
      max-width: 1200px;
      margin: 0 auto;
    }

    .features-block.reverse {
      flex-direction: row-reverse;
      align-items: center;
      justify-content: space-between;
      gap: 60px;
    }

    .features-block {
      flex-direction: row;
      align-items: center;
      gap: 60px;
    }

    .features-text {
      flex: 1.1;
      max-width: 600px;
    }

    .features-title {
      font-size: 42px;
      line-height: 48px;
    }

    .features-image {
      flex: 0.9;
      max-width: 500px;
      width: 100%;
      height: auto;
    }

    .features-icon {
      left: -70px;
    }

    .tech-logo {
      width: 120px;
    }
  }
</style>