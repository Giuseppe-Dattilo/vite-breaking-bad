<script>
export default {
    name: 'SelectForm',
    data() {
        return {
            value: ''
        }
    },
    props: { list: Array },
    emits: ['selected'],
}

</script>

<template>
    <select class="form-select container" v-model="value" @change="$emit('selected', value)">
        <option value="" selected>Tutti</option>
        <option v-for="element in list" :value="element">{{ element }}</option>
    </select>
</template>

<style>

</style>