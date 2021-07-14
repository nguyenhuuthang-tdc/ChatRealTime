<template>
    <h1>{{ titleHeader }}</h1>
</template>

<script>
export default {
    name: "comp-footer",
    props: {
        titleHeader: String
    },
    data() {
        return {
            content: "footer of page",
        }
    },
}
</script>

<style>

</style>
