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
        methods: {
            handle_user_clicked: function(username) {
                this.special_username = username;
            }
        },
        mounted () {
            this.$root.$on(`user_clicked`, this.handle_user_clicked);
        },
    }
</script>

<style scoped>

</style>