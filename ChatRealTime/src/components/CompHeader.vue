<template>
    <header>
        <button v-on:click="changeTitleEvent()">Change title event</button>
        <h1>{{ titleHeader }}</h1>
    </header>
</template>

<script>
export default {
    name: "comp-header",
    props: {
        titleHeader: String,
    },
    data() {
        return {
        }
    },
    methods: {
        changeTitleEvent() {
            this.$emit("changeTitleEvent");
        }
    },
}
</script>

<style>

</style>
