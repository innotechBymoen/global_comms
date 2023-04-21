<template>
    <div>
        <p v-for="(user, i) in users" :key="i" @click="handle_user" :username="user">Welcome, {{ user }}</p>
    </div>
</template>

<script>
/* eslint-disable */
    export default {
        methods: {
            handle_user(details) {
                let username_value = details[`target`].getAttribute(`username`);
                this.$root.$emit(`user_clicked`, username_value);
            }
        },
        data() {
            return {
                users: [`User_One`,`User_Two`,`User_Three`]
            }
        },
    }
</script>

<style scoped>

</style>