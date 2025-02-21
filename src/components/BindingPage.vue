<template>
<h1>
    Binding Component 
</h1>
<div v-html="tag"></div>
<div v-html="button"></div>

</template>
<script>
export default {
    name:'BindingPage',
    data(){
        return{
            tag:"<p>Talha Waleed Just exploring new technology </p>",
            button:"<button> click me </button>"
        }
    }
}
</script>