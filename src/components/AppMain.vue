<script>
import CharactersList from './characters/CharactersList.vue';
export default {
    name: 'AppMain',
    components: { CharactersList },
};

</script>

<template>
    <main class="container">
        <characters-list></characters-list>
    </main>
</template>

<style>

</style>
