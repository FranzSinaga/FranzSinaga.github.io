<template>
    <footer>
        <div class="container">
            <div  class="left-text">
                <h2 class="resume mt-5">Like what you see?</h2>
                <h2 class="resume mt-3">View my <a href="https://drive.google.com/open?id=11XMhaOVMod4Mm0KaXdZyBhqZQX37iX5Y" target="_blank">resume</a>, follow me or contact me</h2>
                <div class="social mt-5">
                    <a class="social" href="mailto:sinagafranz12@gmail.com" style="margin-right: 20px;"><i class="fas fa-2x fa-envelope"></i></a>
                    <a class="social" href="https://medium.com/@sinagafranz12" style="margin-right: 20px;"><i class="fab fa-2x fa-medium-m"></i></a>
                    <a class="social" href="https://github.com/FranzSinaga " style="margin-right: 20px;"><i class="fab fa-2x fa-github"></i></a>
                    <a class="social" href="https://gitlab.com/WzeT?nav_source=navbar" style="margin-right: 20px;"><i class="fab fa-2x fa-gitlab"></i></a>
                    <a class="social" href="https://www.linkedin.com/in/franz-sinaga-4b39b9162/" style="margin-right: 20px;"><i class="fab fa-2x fa-linkedin"></i></a>
                </div>
                <div class="copy mt-4">&copy; {{date.getFullYear()}} FRANZ SINAGA | <a href="mailto:sinagafranz12@gmail.com">sinagafranz12@gmail.com</a></div>
            </div>
        </div>
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
    @import url('https://fonts.googleapis.com/css?family=Nunito+Sans:400,700');
    footer{
        background-color: black;
        padding: 20px;
        margin-bottom: -10px;
    }
    .copy a{
        text-decoration: none;
        color: white;}
    .copy{
        color: white;
        font-family: 'Alegreya Sans SC', sans-serif;
    }
    .left-text{
        text-align: left;
    }
    .resume{
        font-family: 'Nunito Sans', sans-serif;
        font-weight: bolder;
        color: white;
        line-break: normal;
    }
    .resume a{
        color: dodgerblue;
        text-decoration: none;
    }
    .resume a:hover{
        color: #3f63ff;
    }
    .social{
        color: white ;
    }
    .social:hover{color: darkgray}
</style>