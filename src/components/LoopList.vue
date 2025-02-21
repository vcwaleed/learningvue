<template>
<h1>For Loop in Vue Js</h1>
<ul class="a">
    <li v-for="i in technology" :key="i">
        {{ i }}
    </li>
</ul>


<br />
<br />
<ul>
    <li v-for="item in users" :key="item.id">
        {{ item.name }}
        {{ item.email}}
    </li>
</ul>
</template>

<script>
export default {
    name: "LoopList",
    data() {
        return {
            technology: ["talha", "waleed", "muhammad", "Ali", "waleed"],
            users: [{
                    id: 1,
                    name: "Talha1",
                    email: "talha1@gmail.com",
                },
                {
                    id: 2,
                    name: "Talha2",
                    email: "talha2@gmail.com",
                },
                {
                    id: 3,
                    name: "Talha3",
                    email: "talha3@gmail.com",
                },
                {
                    id: 4,
                    name: "Talha4",
                    email: "talha4@gmail.com",
                },
            ]
        };
    },
};
</script>

<style></style>
