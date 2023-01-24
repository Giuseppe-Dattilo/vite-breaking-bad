<script>
import { store } from '../../data/store';
import CharacterCard from './CharacterCard.vue';
export default {
    name: 'CharactersList',
    components: { CharacterCard },
    data() {
        return { store }
    }
};

</script>

<template>
    <section id="characters" class="my-5">
        <div class="row row-cols-2 row-cols-md-3 row-cols-lg-5">
            <character-card class="mb-5" v-for="character in store.characters" :key="character._id"
                :name="character.name" :number="character.number" :img="character.imageUrl" :type="character.type1">
            </character-card>
        </div>
    </section>
</template>

<style lang="scss">

</style>
