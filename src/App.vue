<template>
<HelloWorld msg="Welcome to learn " />
<HomePage/>
<PlayPage message="Waleed do Your Work "/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import HomePage from './components/HomePage.vue'
import PlayPage from './components/PlayPage.vue'

export default {
    name: 'App',
    components: {
        HelloWorld,
        HomePage,
        PlayPage 

    }
}
</script>

