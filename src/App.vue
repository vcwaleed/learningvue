<template>
<HelloWorld msg="Welcome to learn " />
<HomePage/>
<PlayPage message="Waleed do Your Work "/>
<InputPage/>
<CheckBox/>
<LoopList/>
<ChidPage  :user="user" :getdata="getdata"/>
<BindingPage/>
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
        BindingPage

    },
    data(){
        return{
            user:[{name:"talha", email:"talhawaleed@gmail.com"}]
        }
    },
    methods: {
        getdata(){
            console.log("From main function bro ")
        }
    },

}
</script>

