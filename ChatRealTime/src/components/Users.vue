<template>     
    <p>{{ users.name }}</p>
</template>

<script>
export default {
    name: "user",
    props: {
        users: Object,
        default: null
    },
    data() {
        return {
            
        }
    },
}
</script>

<style>

</style>
