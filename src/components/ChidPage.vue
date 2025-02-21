<template>
<h2> child componet </h2>

<ul>
    <li v-for="item in user" :key="item">
        {{ item.name }}
    </li>
</ul>
<button v-on:click="getdata()"> Get data from main componets </button>
<br/>
<br/>
<button v-on:click="username(name)"> get data from child</button>
</template>

<script>
export default {
    name: 'ChidPage',
    data() {
        return {
            name: "talha"

        }
    },
    props: {
        user: Object,
        getdata: Function,
        username: Function,

    }
}
</script>

<style>
</style>
