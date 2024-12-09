<template>
  <p>Reaction Time: {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 200) {
      this.rank = "Wow! Ninja Fingers!";
    } else if (this.score < 300) {
      this.rank = "Rapid Reflexes";
    } else if (this.score < 500) {
      this.rank = "Not Bad";
    } else if (this.score < 700) {
      this.rank = "Not Good";
    } else if (this.score < 1000) {
      this.rank = "So Slow...";
    } else if (this.score < 1500) {
      this.rank = "Better next time...";
    } else {
      this.rank = "Snail Pace...";
    }
  },
};
</script>

<style scoped>
.rank {
  font-size: 1.4rem;
  color: #0faf87;
  font-weight: bold;
}
</style>