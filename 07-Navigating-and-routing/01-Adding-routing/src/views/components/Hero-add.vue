<template>
    <div>
        <h3>Add Hero </h3>

        <form>
        <label for="fname">First name:</label><br>
        <input type="text" id="fname" v-model="hero.fname"><br>

        <label for="lname">Last name:</label><br>
        <input type="text" id="lname" v-model="hero.lname"><br><br>

        <input type="button" value="Submit" v-on:click="submitForm"> &nbsp; &nbsp;
         <input type="button" value="Clear" @click="clearForm">
        </form>

        <h1>First Name {{hero.fname}}</h1>
        <h3>Last Name {{hero.lname}}</h3>

        <h1> Accessing property from object </h1>
        {{messageFname}}
        {{messageLname}}

    </div>
</template>

<script>
    export default {
        name:'HeroAdd',
        data() {
            return {
                messageFname: "",
                message:"",
                messageLname: "",
                hero:{
                    fname:'',
                    lname:''
                }
            }
        },
        methods: {
            submitForm() {
                this.messageFname=this.hero.fname;
                this.messageLname=this.hero.lname
            },
            clearForm(){
                this.message="Clear Form button is clicked";
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>