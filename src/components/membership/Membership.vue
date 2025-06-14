<template>
  <section class="membership">
    <h2 class="membership-title">Membership options</h2>

    <div class="membership-cards">
      <MembershipCard
        title="Starter"
        price="$19"
        perMonth="/month"
        :features="starterFeatures"
        buttonLabel="Subscribe now"
        variant="starter"
      />

      <MembershipCard
        title="Pro"
        price="$29"
        perMonth="/month"
        :features="proFeatures"
        buttonLabel="Subscribe now"
        variant="pro"
      />

      <MembershipCard
        title="Enterprise"
        price="Custom"
        :features="enterpriseFeatures"
        buttonLabel="Talk to us"
        variant="enterprise"
      />
    </div>

    <Testimonial
      text="This book club transformed my technical reading from a solitary activity into an enriching community experience. The discussions are gold!"
      author="Sarah Chen, Software Architect"
    />
  </section>
</template>

<script setup>
  import MembershipCard from "@/components/membership/card/MembershipCard.vue";
  import Testimonial from "@/components/membership/testimonial/Testimonial.vue";

  const starterFeatures = ["1 book/month", "Online forums"];
  const proFeatures = ["2 books/month", "Virtual meetups"];
  const enterpriseFeatures = ["Team access", "Private sessions"];
</script>

<style scoped>
  .membership {
    display: flex;
    flex-direction: column;
    gap: 30px;
    padding: 60px 20px;
  }

  .membership-title {
    font-family: "Martian Mono", monospace;
    font-size: 26px;
    line-height: 34px;
    color: rgb(6, 38, 48);
    margin: 0;
  }

  .membership-cards {
    display: flex;
    flex-direction: column;
    gap: 24px;
  }

  @media (min-width: 768px) {
    .membership {
      padding: 40px;
    }

    .membership-title {
      font-size: 32px;
      line-height: 40px;
    }

    .membership-cards {
      flex-direction: row;
      flex-wrap: wrap;
      gap: 24px;
      justify-content: flex-start;
    }
  }

  @media (min-width: 1440px) {
    .membership {
      padding: 40px 180px;
      gap: 40px;
    }

    .membership-title {
      font-size: 42px;
      line-height: 54px;
      text-align: center;
    }

    .membership-cards {
      flex-wrap: nowrap;
      justify-content: space-between;
    }
  }
</style>