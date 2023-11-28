<script>
import { store } from '../store';
import AppCard from './AppCard.vue';

export default {
    data() {
        return {
            store,
        }
    },
    components: {
        AppCard
    }
};
</script>

<template>
    <div class="ms_container">
        <div class="ms_container-1">
            <h5 class="fw-bolder text-bg-dark p-2">Found 20 cards</h5>
            <div class="row row-cols-5">
                <div class="col mb-4" v-for="card in store.cards" key="card.id">
                    <AppCard :card="card" />
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;

 .ms_container {
    background-color: $orange;
    padding: 4rem;
    .ms_container-1 {
        background-color: white;
        padding: 3rem;
        margin-top: 2rem;
    }
}

</style>