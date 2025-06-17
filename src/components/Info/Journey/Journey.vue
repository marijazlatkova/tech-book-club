<template>
  <section class="journey">
    <div class="journey-wrapper">
      <h2 class="journey-title">Your tech <span class="break">reading journey</span></h2>

      <div class="steps">
        <div v-for="(step, index) in steps" :key="index">

          <div class="step">
            <div class="step-wrapper">
              <div class="step-number">{{ index + 1 }}</div>
              <img v-if="index < steps.length -1" :src="arrowIcon" class="arrow" alt="Arrow Icon" />
            </div>
            <p class="step-text">{{ step }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
  import arrowIcon from "@/assets/images/pattern-arrow.svg";

  const steps = [
    "Choose your membership tier",
    "Get your monthly book selection",
    "Join our discussion forums",
    "Attend exclusive meetups",
  ];
</script>

<style scoped>
  .journey {
    padding: 10px 20px;
  }

  .journey-wrapper {
    background-color: rgb(250, 245, 243);
    background-image: url("@/assets/images/pattern-light-bg.svg"), url("@/assets/images/pattern-glow.svg");
    background-position: top left, top right;
    display: flex;
    border-radius: 20px;
    padding: 40px 30px;
    flex-direction: column;
    gap: 24px;
  }

  .journey-title {
    font-family: "Martian Mono", monospace;
    font-size: 26px;
    line-height: 34px;
  }

  .break {
    display: inline;
  }

  .steps {
    display: flex;
    flex-direction: column;
    gap: 14px;
  }

  .step {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 8px;
  }

  .step-wrapper {
    display: flex;
    gap: 80px;
  }

  .step-number {
    font-family: "Martian Mono", monospace;
    border: 2.4px solid rgb(6, 38, 48);
    padding: 4px 8px;
    border-radius: 5px;
    font-weight: 600;
  }

  .step-text {
    font-family: "Martian Mono", monospace;
    font-size: 16px;
    font-weight: 600;
    color: rgb(6, 38, 48);
  }

  .arrow {
    display: none;
    width: 70px;
    height: auto;
  }

  @media (min-width: 768px) {
    .journey {
      padding: 40px;
    }

    .journey-wrapper {
      padding: 40px;
    }

    .journey-title {
      font-size: 32px;
      line-height: 40px;
    }
  }

  @media (min-width: 1440px) {
    .journey {
      padding: 60px 180px;
    }

    .journey-wrapper {
      padding: 60px;
    }

    .journey-title {
      font-size: 42px;
      line-height: 54px;
      text-align: center;
    }

    .break {
      display: block;
    }

    .steps {
      flex-direction: row;
      justify-content: space-between;
      gap: 40px;
    }

    .arrow {
      display: block;
    }
  }
</style>