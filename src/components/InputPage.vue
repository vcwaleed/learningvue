<template>
<h1>Input Value Section </h1>
<div class="text_fields">
    <input type="text" placeholder="Enter Your Email" v-model="email" />
    <input type="password" placeholder="Enter Your Passwords" v-model="password" />
    <button type="button" v-on:click=" getdata()">Get the data </button>
</div>
</template>

<script>
export default {
    name: 'InputPage',
    data() {
        return {
            email: '',
            password: '',
        }
    },
    methods: {
        getdata() {
            console.log(this.email);
            console.log(this.password);
        }
    },
}
</script>

<style>
.text_fields {
    display: flex;
    width: 420px;
    flex-direction: column;
    gap: 10px;
}
</style>
