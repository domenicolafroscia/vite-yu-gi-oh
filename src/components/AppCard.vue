<script>
export default {
    props: {
        card: Object,

    }
}
</script>

<template>
    <div class="card mb-4">
        <img :src="card.card_images[0].image_url" alt="">
        <h4 class="text-center text-white my-3">{{ card.name }}</h4>
        <p class="text-center">{{ card.archetype }}</p>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;

.card {
    background-color: $orange;
  
}
</style>