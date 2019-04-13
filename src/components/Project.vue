<template>
    <div style="background-color: azure">
        <div class="canhide container">
            <div class="row" id="about">
                <div class="col-md-10 offset-md-1">
                    <div class="row mt-4">
                        <div class="col-md-3">
                            <h1 class="text-md-right famyly-open-sans" style="letter-spacing: 5px;">Selected<br>Projects<hr></h1>
                            <p></p>
                        </div>
                        <div class="col-md-7">
                            <div class="mb-5 text-break famyly-open-sans" style="text-align: left; font-size: 25px">
                                <div class="card mb-4" v-for="project in projects" :key="project.title">
                                    <div class="card-body">
                                        <h5 class="card-title">{{project.title}}</h5>
                                        <p class="card-text">{{project.desc}}</p>
                                        <a v-bind:href="project.linkUrl" class="card-link" target="_blank" v-if="project.link">Look Project</a>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Project",
        data(){
            return{
                projects: [
                    {
                        title: "Cerdas (Android Mobile Application)",
                        desc: "Helping students discuss lessons at school. developed using Android Studio and Firebase. Build " +
                            "for android user",
                        link: false,
                        linkUrl: ""
                    },
                    {
                        title: "Build Del FM radio website. ",
                        desc: "Build Del FM radio website. ",
                        link: true,
                        linkUrl: "http://radiodelfm.co.id/"
                    },
                    {
                        title: "Build TEF (Toba Entrepreneurship Festival) 2018 ",
                        desc: "Build static website for Toba Entrepreneurship Festival that held in Institut Teknologi Del 2018. This is the first TEF event in IT Del",
                        link: true,
                        linkUrl: "http://tef2018.co.id/"
                    },
                ]
            }
        }
    }
</script>

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
</style>