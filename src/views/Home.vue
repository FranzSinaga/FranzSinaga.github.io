<template>
    <div>
        <div class="containerss">
            <h1 class="canhide welcomeTextPosition h1-special family-VT">
                Franz Sinaga<hr color="white" >Software Engineer<br>
                <div style="margin-top: 20px;">
                    <a class="social" href="https://medium.com/@sinagafranz12" style="margin-right: 10px;"><i class="fab fa-medium-m"></i></a>
                    <a class="social" href="https://github.com/FranzSinaga " style="margin-right: 10px;"><i class="fab fa-github"></i></a>
                    <a class="social" href="https://gitlab.com/WzeT?nav_source=navbar" style="margin-right: 10px;"><i class="fab fa-gitlab"></i></a>
                    <a class="social" href="https://www.linkedin.com/in/franz-sinaga-4b39b9162/" style="margin-right: 10px;"><i class="fab fa-linkedin"></i></a>
                </div>
            </h1>

            <section class="demo canhide">
                <a href="#about"><span></span></a>
            </section>
        </div>
        <div style="background-color: azure">
            <div class="canhide container">
                <div class="row" id="about">
                    <div class="col-md-10 offset-md-1">
                        <div class="row mt-4">
                            <div class="col-md-3">
                                <h1 class="text-md-right famyly-open-sans" style="letter-spacing: 10px;">About<br> Me<hr></h1>
                            </div>
                            <div class="col-md-7">
                                <div class="mb-5 text-break famyly-open-sans" style="text-align: left; font-size: 25px">
                                    <h1 class="mt-2">Hello There,</h1>
                                    <div class="mt-3">
                                        My name is Franz Aditya Natanael Sinaga. I am a student at the Del Institute of Technology.
                                        I am happy to learn new things about technology, especially in the field of software engineer
                                        I like writing code. I wrote the code for my study and directed myself to work in the IT world according to my interests.
                                        I like to work with other people to get things done. If you love to share something to me, feel free to reach me.
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <Projects></Projects>
<!--            <div class="row" id="blog">-->
<!--                <div class="col-md-10 offset-md-1">-->
<!--                    <div class="row mt-4">-->
<!--                        <div class="col-md-3">-->
<!--                            <h1 class="text-md-right " style="letter-spacing: 10px;">Latest<br> Blog</h1>-->
<!--                        </div>-->
<!--                        <div class="col-md-7">-->
<!--                            <div v-for="article in articles.items.slice(0,2)" :key="article.id">-->
<!--                                <Article :article="article" />-->
<!--                            </div>-->
<!--                            <div class=" canhide">-->
<!--                                <a target="_blank" href="https://medium.com/@sinagafranz12" class="btn btn-lg btn-outline-success btn-block" style="padding: 6.375px;">-->
<!--                                    <i class="fab fa-medium-m"></i> Look More At Medium-->
<!--                                </a>-->
<!--                                <br>-->
<!--                            </div>-->
<!--                        </div>-->
<!--                    </div>-->
<!--                </div>-->
<!--            </div>-->
        </div>
    </div>
</template>
<script>
    import Article from '@/components/Article.vue'
    import Projects from '@/components/Project.vue'
    import Axios from 'axios'
    export default {
        name: "Home",
        components: {Article,Projects},
        mounted(){
            this.getArticles();
        },
        data(){
            return{
                articles: {},
            }
        },
        methods: {
            getArticles(){
                Axios.get('https://api.rss2json.com/v1/api.json?rss_url=https%3A%2F%2Fmedium.com%2Ffeed%2F%40sinagafranz12')
                    .then(response => {
                        this.articles = response.data
                    })
            }
        }
    }
</script>
<style>
    @import url('https://fonts.googleapis.com/css?family=Archivo+Black');
    @import url('https://fonts.googleapis.com/css?family=Open+Sans:300,700');
</style>
<style scoped>

    .family-VT{
        font-family: 'Archivo Black', sans-serif;
        /*font-weight: bolder;*/
        letter-spacing: 3px;
    }
    a{
        text-decoration: none;
    }
    .famyly-open-sans{ font-family: 'Open Sans', sans-serif;}

    .welcomeTextPosition{
        position: absolute;
        top: 30%;
        left: 50%;
        /*font-size: 2.5em;*/
        color: white;
    }
    .position-logo{
        padding-top: 30%;
    }
    .social{
        color: aliceblue;
    }
    .social:hover{
        color: lightslategray;
    }
    .explore-me-text{
        position: absolute;
        top: 70%;
        color: white;
        left: 50%;
    }
    .btn-down{
        /*position: absolute;*/
        top: 75%;
    }
    .containerss {
        height: 100vh;
        margin-top: -60px;
        /*background: #141E30;  !* fallback for old browsers *!*/
        /*background: -webkit-linear-gradient(to right, #243B55, #141E30);  !* Chrome 10-25, Safari 5.1-6 *!*/
        /*background: linear-gradient(to right, #243B55, #141E30); !* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ *!*/
        /*background-image: url('https://ak0.picdn.net/shutterstock/videos/26916550/thumb/1.jpg');*/
        background-image: url("https://i.ytimg.com/vi/aYIlKchp7AU/maxresdefault.jpg");
        background-size: cover;
    }

    /*scroll down*/
    a span {
        position: absolute;
        top: 80%;
        left: 50%;
        width: 24px;
        height: 24px;
        margin-left: -12px;
        border-left: 1px solid #fff;
        border-bottom: 1px solid #fff;
        -webkit-transform: rotate(-45deg);
        transform: rotate(-45deg);
        -webkit-animation: sdb 1.5s infinite;
        animation: sdb 1.5s infinite;
        box-sizing: border-box;
    }
    @-webkit-keyframes sdb {
        0% {
            -webkit-transform: rotate(-45deg) translate(0, 0);
            opacity: 0;
        }
        50% {
            opacity: 1;
        }
        100% {
            -webkit-transform: rotate(-45deg) translate(-20px, 20px);
            opacity: 0;
        }
    }
    @keyframes sdb {
        0% {
            transform: rotate(-45deg) translate(0, 0);
            opacity: 0;
        }
        50% {
            opacity: 1;
        }
        100% {
            transform: rotate(-45deg) translate(-20px, 20px);
            opacity: 0;
        }
    }
</style>
