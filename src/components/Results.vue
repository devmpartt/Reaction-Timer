<template>
  <p>Reaction time - {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      rank : null
    }
  },
  mounted() {
    if (this.score < 250) {
      this.rank = 'Great'
    } else if (this.score < 400) {
      this.rank = 'Developable'
    } else {
      this.rank = '...weak'
    }
  }
}
</script>

<style>
  .rank {
    font-size: 1.4em;
    color: #af0f4c;
    font-weight: bold;
  }
</style>