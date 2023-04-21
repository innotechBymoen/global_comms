<template>
    <div>
        <p v-for="(user, i) in users" :key="i" @click="details => $root.$emit(`user_clicked`, user)" >Welcome, {{ user }}</p>
    </div>
</template>

<script>
/* eslint-disable */
    export default {
        data() {
            return {
                users: [`User_One`,`User_Two`,`User_Three`]
            }
        },
    }
</script>

<style scoped>

</style>