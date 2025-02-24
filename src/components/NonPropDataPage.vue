<template>
    <h1 v-bind="$attrs">Non prop Page</h1>
    <p>Talha</p>
    <p>Waleed</p>
    <p>{{ data }}</p>
</template>
<script>
export default {
    name: "NonPropDataPage",
    props:{
        data:String
    }
};
</script>
