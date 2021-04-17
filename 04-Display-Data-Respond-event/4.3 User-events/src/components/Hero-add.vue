<template>
    <div>
        <h3>Add Hero </h3>

        <form>
        <label for="fname">First name:</label><br>
        <input type="text" id="fname" name="fname"><br>

        <label for="lname">Last name:</label><br>
        <input type="text" id="lname" name="lname"><br><br>

        <input type="button" value="Submit" v-on:click="submitForm"> &nbsp; &nbsp;
         <input type="button" value="Clear" @click="clearForm">
        </form>

        <h1>Event {{message}}</h1>
    </div>
</template>

<script>
    export default {
        name:'HeroAdd',
        data() {
            return {
                message: ""
            }
        },
        methods: {
            submitForm() {
                this.message="Submit Form button is clicked";
            },
            clearForm(){
                this.message="Clear Form button is clicked";
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>