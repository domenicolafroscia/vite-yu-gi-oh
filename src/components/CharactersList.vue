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
        <select class="form-select w-25 ms-3" aria-label="Default select example">
            <option selected>Open this select menu</option>
            <option value="1">One</option>
            <option value="2">Two</option>
            <option value="3">Three</option>
        </select>

        <div class="ms_container-1">
            <h5 class="fw-bolder text-bg-dark p-2">Found 20 cards</h5>
            <div class="row row-cols-5">
                <div class="col" v-for="card in store.cards">
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
    padding: 5rem;
    .ms_container-1 {
        background-color: white;
        padding: 3rem;
        margin-top: 2rem;
    }
}


</style>