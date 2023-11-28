<script>
import { store } from '../store';

export default {
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="ms_container">
        <select v-model.trim="store.selectCards" @change="$emit('cardSelect')" class="form-select w-25 ms-3"
            aria-label="Default select example">
            <option selected></option>
            <option value="Alien">Alien</option>
            <option value="Ally of Justice">Ally of Justice</option>
            <option value="Ancient Gear">Ancient Gear</option>
        </select>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;

.ms_container {
    background-color: $orange;
    padding: 5rem 5rem 0 5rem;

}
</style>

        





