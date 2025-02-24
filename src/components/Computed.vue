<template>
<h1>Computed Proporties</h1>
<sapn> Total doller ${{ dollors }}</sapn>
<br/>
<span>Rs  {{ rupee}}</span>
<br/>
<span> Discount {{ discountPrice }}</span>

</template>
<script>

export default{
    name:'ComputedPage',
    data(){
        return{
            dollors:100,
            rupeeVal:270,
            discount:10,
        }
    },
    computed:{
        rupee(){
            return this.dollors * this.rupeeVal;
        },
        discountPrice(){
            return this.dollors - this.discount;
        }
    }


}

</script>