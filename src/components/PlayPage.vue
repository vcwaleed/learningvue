<template>
<div>
    <span class="heading"> Hi this is my PlayPage for the development {{ email }}</span>
    <p>Mobile {{ number }}</p>
    <p>{{message}}</p>
 
    <span> Name : {{ getname(11) }}</span> <br />
    

    <br />
    <div class="btn">
       
        <button v-on:click=" test2()">Click me</button>
        <button v-on:click=" getemail()">Click me</button>
    </div>


</div>
<input type="number" v-model="number"/>
</template>
<script>
export default {
    name: 'PlayPage',
    props: {
        message: String,
    },
    data() {
        return {
            email: "talhawaleed@gmail.com",
            number: 9999,
            getname: (name) => {
                return (name)
            }
        }
    },
    methods: {
        getemail(){
            
                this.number=this.number+1;
               
            
           
          
        },
        test2() {
            alert("this is working function ");
        }
    },
}
</script>
<style scoped>
.heading {
    font-size: larger;
    color: blue;

    background-color: aquamarine;
}
.btn {
    width: 200px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    gap: 10px;
}
</style>
