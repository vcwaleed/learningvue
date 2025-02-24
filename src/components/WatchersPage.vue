<template>
<h1>Watcher Proporties</h1>
<button v-on:click="decrement()" class="btn"> - </button>
<span> {{count}}</span>
<button v-on:click="increment()"  class="btn"> + </button>

</template>
<script>
export default{
    name:'watchersPage',
    data(){
        return{
            count:0,
        }
    },
    methods:{
        increment(){
            this.count++;
        },
        decrement(){
            this.count--;
        },

    },
    watch:{
        count(val,oldval){
            console.log("old value is ",oldval);
            if(val>5 && val>oldval){
                alert("Count is greater than 5");
                this.count=0;
            }
            console.log("New Value is ",val);
        }
    }

}
</script>
<style scoped>
h1{
    color:blue;
}
.btn{
    background-color:blue;
    color:white;
    padding:10px;
    padding-left: 100px;
    padding-right: 100px;
    margin:10px;
    border-radius:5px;
}
</style>