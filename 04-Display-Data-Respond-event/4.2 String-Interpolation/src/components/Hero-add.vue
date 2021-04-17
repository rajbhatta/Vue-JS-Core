<template>
    <div>
        <h3>Add Hero </h3>

        <form action="/action_page.php">
        <label for="fname">First name:</label><br>
        <input type="text" id="fname" name="fname"><br>

        <label for="lname">Last name:</label><br>
        <input type="text" id="lname" name="lname"><br><br>

        <input type="button" value="Submit"> &nbsp; &nbsp;
         <input type="button" value="Clear">
        </form>

    </div>
</template>

<script>
    export default {
        name:'HeroAdd'
    }
</script>

<style lang="scss" scoped>

</style>