<template>
    <div>
        <h1>{{ special_username }}</h1>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                special_username: undefined
            }
        },
        mounted () {
            this.$root.$on(`user_clicked`, username =>  this.special_username = username );
        },
    }
</script>

<style scoped>

</style>