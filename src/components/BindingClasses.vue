<template>
<h1 :class="{green:colorfull}">Binding Classes in Vue js </h1>
<button v-on:click=" toggle()">click to change the color</button>
</template>
<script>
export default {
    name:'BindingClasses',
    data(){
        return{
            colorfull:true,
        }
    },
    methods:{
        toggle(){
            this.colorfull=!this.colorfull;
        }
    }



}
</script>
<style>
.green{
    background-color: chartreuse;
    width: 400px;
    padding: 10px;

}
</style>