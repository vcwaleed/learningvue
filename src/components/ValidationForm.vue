<template>
<h1>Valdation Form</h1>
<h2>Form Modifiers</h2>
<input type="text" v-model="data"/>
<h5>Data is {{data}}</h5>
</template>

<script>
export default{
    name:'ValidationForm',
    data(){
        return{
            data:'',
        }
    }

}
</script>