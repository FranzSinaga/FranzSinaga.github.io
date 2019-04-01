<template>
    <footer>
        <div class="logo"></div>
        <div class="copy">&copy; {{date.getFullYear()}} FRANZ SINAGA | sinagafranz12@gmail.com</div>
    </footer>
</template>

<script>
    export default {
        name: "Footer",
        data(){
            return{
                date: new Date(),
            }
        }
    }
</script>

<style scoped>
    @import url('https://fonts.googleapis.com/css?family=Alegreya+Sans+SC');
    footer{
        background-color: black;
        padding: 20px;
        margin-bottom: -10px;
    }
    .copy{
        color: white;
        font-family: 'Alegreya Sans SC', sans-serif;
    }
</style>