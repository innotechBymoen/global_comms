<template>
    <div>
        <div v-for="(user,i) in users" :key="i">
            <h4>{{ user[`first_name`] }}, {{  user[`last_name`] }}</h4>
            <h6>{{ user[`email`] }}</h6>
        </div>
        <h5>{{ error_message }}</h5>
    </div>
</template>

<script>
import axios from 'axios';
    export default {
        data() {
            return {
                users: undefined,
                error_message: undefined
            }
        },
        mounted () {
            axios.request({
                url: `https://reqres.in/api/users`
            }).then((response) => {
                this.users = response[`data`][`data`];
            }).catch((error) => {
                error;
                this.error_message = `Sorry, please try again!`
            });
        },
    }
</script>

<style scoped>

</style>