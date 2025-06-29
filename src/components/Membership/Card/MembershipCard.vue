<template>
  <div class="membership-card" :class="variant">
    <h3 class="card-title">{{ title }}</h3>
    <p class="card-price">
      {{ price }}
      <span v-if="perMonth" class="per-month">{{ perMonth }}</span>
    </p>
    <hr class="separator" />
    <ul class="card-features">
      <li v-for="feature in features" :key="feature" class="card-feature">
        <img :src="checkIcon" class="check-icon" alt="Check icon" />
        {{ feature }}
      </li>
    </ul>
    <a href="#footer" class="card-button">{{ buttonLabel }}</a>
  </div>
</template>

<script setup>
  import checkIcon from "@/assets/images/icon-check.svg";

  defineProps({
    title: String,
    price: String,
    perMonth: String,
    features: Array,
    buttonLabel: String,
    variant: String,
  });
</script>

<style scoped>
  .membership-card {
    display: flex;
    flex-direction: column;
    gap: 30px;
    border: 1px solid rgb(210, 210, 210);
    border-radius: 10px;
    padding: 30px;
  }

  .membership-card.pro {
    background: rgb(250, 245, 243) url("@/assets/images/pattern-glow.svg") left;
  }

  .card-title {
    font-family: "Martian Mono", monospace;
    font-size: 22px;
    font-weight: 600;
    color: rgb(6, 38, 48);
    margin: 0;
  }

  .card-price {
    font-family: "Martian Mono", monospace;
    font-size: 28px;
    font-weight: 700;
    color: rgb(6, 38, 48);
    margin: 0;
    display: flex;
    align-items: center;
  }

  .per-month {
    font-size: 18px;
    font-weight: 300;
    color: rgb(56, 81, 89);
    margin-left: 5px;
  }

  .separator {
    border: none;
    border-top: 1px solid rgb(210, 210, 210);
    margin: 5px 0;
  }

  .card-features {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 20px;
    width: 100%;
    font-size: 20px;
    list-style: none;
    color: rgb(56, 81, 89);
    padding: 0;
    margin: 0;
  }

  .card-feature {
    display: flex;
    align-items: center;
    gap: 15px;
  }

  .check-icon {
    width: 16px;
    height: 16px;
  }

  .card-button {
    font-family: "Martian Mono", monospace;
    font-size: 18px;
    font-weight: 600;
    text-transform: uppercase;
    text-align: center;
    text-decoration: none;
    width: 100%;
    background-color: rgb(255, 245, 239);
    color: rgb(6, 38, 48);
    border: 2px solid rgb(6, 38, 48);
    border-radius: 8px;
    padding: 22px;
    cursor: pointer;
  }

  .card-button:hover {
    background: no-repeat linear-gradient(90deg, rgb(255, 226, 209), rgb(255, 245, 239));
    transition: 200ms;
  }

  @media (min-width: 768px) {
    .membership-card {
      flex: 0 1 calc(50% - 12px);
      max-width: calc(50% - 12px);
    }

    .membership-card.enterprise {
      flex-basis: calc(50% - 12px);
      max-width: calc(50% - 12px);
    }
  }

  @media (min-width: 1440px) {
    .membership-card,
    .membership-card.enterprise {
      flex: 1;
    }
  }
</style>