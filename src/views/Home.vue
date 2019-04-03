<template>
    <div>
        <div class="containerss">
            <h1 class="canhide welcomeTextPosition h1-special family-VT">
                FRANZ SINAGA<hr color="white" >{Software Engineer}<br>
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
                            <div class="col-md-4">
                                <h1 class="text-md-right " style="letter-spacing: 10px;">ABOUT<br> ME</h1>
                            </div>
                            <div class="col-md-6">
                                <p class="mb-5 text-break" style="text-align: left; font-size: 25px">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
<!--            <div v-for="article in articles.items" :key="article.id">-->
<!--                <Article :article="article" />-->
<!--            </div>-->
        </div>
    </div>
</template>
<script>
    import Article from '@/components/Article.vue'
    import Axios from 'axios'
    // import Article from "../components/Article";
    export default {
        name: "Home",
        components: {Article},
        mounted(){
            this.getArticles();
        },
        data(){
            return{
                articles: {}
            }
        },
        methods: {
            getArticles(){
                Axios.get('https://api.rss2json.com/v1/api.json?rss_url=https%3A%2F%2Fmedium.com%2Ffeed%2F%40sinagafranz12')
                    .then(response => {
                        console.log(response)
                        this.articles = response.data
                    })

            }
        }
    }
</script>

<style scoped>
    @import url('https://fonts.googleapis.com/css?family=Archivo+Black');
    @import url('https://fonts.googleapis.com/css?family=Open+Sans:300,700');
    .family-VT{
        font-family: 'Archivo Black', sans-serif;
        font-weight: bolder;
        letter-spacing: 3px;
    }
    .famyly-open-sans{ font-family: 'Open Sans', sans-serif;}

    .welcomeTextPosition{
        position: absolute;
        top: 30%;
        left: 50%;
        /*font-size: 2.5em;*/
        color: white;
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
        background: #141E30;  /* fallback for old browsers */
        background: -webkit-linear-gradient(to right, #243B55, #141E30);  /* Chrome 10-25, Safari 5.1-6 */
        background: linear-gradient(to right, #243B55, #141E30); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
    }

    /*scroll down*/
    a {
        padding-top: 70px;
    }
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
