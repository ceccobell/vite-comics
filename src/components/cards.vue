<template>
    <div class="col-2 p-3" v-for="card, index in cards">
        <img :src="card.thumb" alt="" class="img-card">
        <h6 class="text-white text-uppercase mt-2">{{ card.series }}</h6>
    </div>
</template>

<script>
export default {
  props: {
    cards: Array
  }
}
</script>

<style scoped>
.img-card {
    width: 100%;
    height: 250px;
    object-fit: cover;
    object-position: top;
}
</style>
