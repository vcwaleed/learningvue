<template>
<h2> child componet </h2>

<ul>
    <li v-for="item in user" :key="item">
        {{ item.name }}
    </li>
</ul>
<button v-on:click="getdata()"> Get data from main componets </button>
</template>
<script>
export default{
    name:'ChidPage',
    props:{
        user:Object,
        getdata:Function,

    }
    }
</script>

<style>
</style>