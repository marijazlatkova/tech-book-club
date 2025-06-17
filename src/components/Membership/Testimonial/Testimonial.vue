<template>
  <div class="testimonial">
    <div class="stars">
      <img v-for="n in 5" :key="n" :src="starIcon" class="star" alt="Star" />
    </div>
    <p class="testimonial-text">{{ text }}</p>
    <p class="testimonial-author">{{ author }}</p>
  </div>
</template>

<script setup>
  import starIcon from "@/assets/images/icon-star.svg";

  defineProps({
    text: String,
    author: String,
  });
</script>

<style scoped>
  .testimonial {
    display: flex;
    flex-direction: column;
    gap: 12px;
    padding-top: 20px;
  }

  .stars {
    display: flex;
    gap: 4px;
  }

  .star {
    width: 30px;
  }

  .testimonial-text {
    font-family: "Martian Mono", monospace;
    font-size: 18px;
    font-weight: 600;
    color: rgb(6, 38, 48);
  }

  .testimonial-author {
    font-family: "Martian Mono", monospace;
    font-size: 14px;
    color: rgb(56, 81, 89);
  }

  @media (min-width: 768px) {
    .star {
      width: 40px;
    }

    .testimonial-text {
      font-size: 20px;
    }

    .testimonial-author {
      font-size: 18px;
    }
  }

  @media (min-width: 1440px) {
    .testimonial {
      align-items: center;
    }

    .testimonial-text {
      font-size: 22px;
    }

    .testimonial-author {
      font-size: 18px;
    }
  }
</style>