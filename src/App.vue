<template>
<ValidationForm/>
<FormPage/>
<br/>
<br/>

<RefPage/>
    <h1>Data from child compoent </h1>
    <h2>{{ childdata }}</h2>

<HelloWorld msg="Welcome to learn " />
<HomePage/>
<PlayPage message="Waleed do Your Work "/>
<InputPage/>
<CheckBox/>
<LoopList/>
<ChidPage  :user="user" :getdata="getdata" :username=" getusername"/>
<BindingPage/>
<BindingClasses/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import HomePage from './components/HomePage.vue'
import PlayPage from './components/PlayPage.vue'
import InputPage from './components/InputPage.vue'
import CheckBox from './components/CheckBox.vue'
import LoopList from './components/LoopList.vue'
import ChidPage from './components/ChidPage.vue'
import BindingPage from './components/BindingPage.vue'
import BindingClasses from './components/BindingClasses.vue'
import RefPage from './components/RefPage.vue'
import FormPage from'./components/FormPage.vue'
import ValidationForm from './components/ValidationForm.vue'


export default {
    name: 'App',
    components: {
        HelloWorld,
        HomePage,
        PlayPage,
        InputPage,
        CheckBox,
        LoopList,
        ChidPage,
        BindingPage,
        BindingClasses,
        RefPage,
        FormPage,
        ValidationForm

    },
    data(){
        return{
            user:[{name:"talha", email:"talhawaleed@gmail.com"}],
            childdata:"",

        }
    },
    methods: {
        getdata(){
            console.log("From main function bro ")
        },
        getusername(name){
            this.childdata=name;
        }
    },

}
</script>

