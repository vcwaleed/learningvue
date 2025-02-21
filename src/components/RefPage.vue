<template>
    <h1>This is Ref componets </h1>

    <input type="text" ref="input"/>
    <button v-on:click="getData()">Click Me</button>
    </template>
    <script>
    export default{
        name:'RefPage',
        methods:{
            getData(){
                this.$refs.input.focus();
                let val=this.$refs.input.value;
                console.log(val)
            }
        }
    }
    </script>