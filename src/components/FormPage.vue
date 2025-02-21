<template>
<h1>Form In Vue Js</h1>
<ul>
    <li v-for="item in error" v-bind:key="item">
        {{ item }} not valid 
    </li>
</ul>
<form>
    <lable>Email : </lable>
    <input type="text" placeholder="enter Your Email" ref="email" v-model="form.email" />
    <br /><br />
    <lable>Password : </lable>
    <input type="password" placeholder="Enter Your Password" ref="password" v-model="form.password" />
    <br /><br />
    <select v-model="form.country">
        <option>Pakistan</option>
        <option>India</option>
        <option>US</option>
        <option>UK</option>
    </select>
    <br />
    <br />
    <lable>Gender</lable>
    <br />
    <label for="male">Male</label>
    <input type="radio" name="w" value="male" id="male" v-model="form.gender" />
    <label for="female">Female</label>
    <input type="radio" name="w" value="female" id="female" v-model="form.gender" />
    <br />
    <br />
    <span>Technology</span>
    <br />
    <label for="javascript">javascript</label>
    <input type="checkbox" value="javascript" v-model="form.technology" id="javascript" />
    <label for="java">java</label>
    <input type="checkbox" value="java" v-model="form.technology" id="java" />
    <label for="python">python</label>
    <input type="checkbox" value="python" v-model="form.technology" id="python" />
    <br />
    <br />

    <button type="button" v-on:click="login()">Submiitted</button>
</form>
<br />
<br />
{{ form }}
</template>

<script>
export default {
    name: "FormPage",
    data() {
        return {
            form: {
                email: "",
                password: "",
                country: "",
                technology: [],
                gender: "",
            },
            error:[],
        };
    },
    methods: {
        login() {
            this.error=[];
            for(const item in this.form){
                if(this.form[item]=== " " || this.form[item].length === 0){
                    this.error.push(item)

                }
               
            }
            if(this.error.length === 0){
                    alert("data submiited successfully ");
                }
            console.warn("login data ", this.form ,this.error);
        },
    },
};
</script>
