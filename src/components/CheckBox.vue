<template>
<h3>Check Box Section</h3>
<label for="java">Java</label>
<input type="checkbox" value="java" v-model="technology" id="java" />
<label for="php">Php</label>
<input type="checkbox" value="php" v-model="technology" id="php" />
<label for="js">Java Script </label>
<input type="checkbox" value="javascript" v-model="technology" id="js" />
<p>Technology : {{ technology }}</p>
<h4>Radio Butoon</h4>
<h3>Who I Am</h3>
<br />
<label for="student">Student</label>
<input type="radio" value="student" name="w" v-model="profession" id="student" />
<label for="teacher">Teacher</label>
<input type="radio" value="teacher" name="w" v-model="profession" id="teacher" />
<p>Your profession {{ profession }}</p>

<h2>Conditional Randering </h2>
<div v-if="weare">
    <p>
        You are right about this person
    </p>
</div>
<div v-else>
    <p>
        You are wrong about this person
    </p>
</div>
<button v-on:click=" toggle()">change opion by function</button>
<br />
<br />
<button v-on:click="weare=!weare">change opion by button </button>
</template>

<script>
export default {
    name: "CheckBox",
    data() {
        return {
            technology: [],
            profession: null,
            weare: false,
        };
    },
    methods: {
        toggle() {
            this.weare = !this.weare;
        }
    },
};
</script>

<style></style>
