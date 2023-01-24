<script>
export default {
    name: 'CharacterCard',
    props: {
        name: String,
        number: Number,
        img: String,
        type: String,
    }
};

</script>

<template>
    <div class="text-center p-2 character-card rounded-4">
        <img class="img-fluid my-5" :src="img" :alt="name">
        <div class="number">{{ number }}</div>
        <h4 v-text="name"></h4>
        <div class="type">{{ type }}</div>

    </div>
</template>

<style scoped lang="scss">
.character-card {
    background-color: white;
    min-height: 300px;
    border: 2px solid black;


    img {
        width: 80px;
    }
}
</style>
