<template>
    <div style="background-color: azure">
        <div class="canhide container" id="blog">
            <div class="mx-auto" style="width:100%; max-width:700px;">
                <div class="card" style="margin-bottom: 10px;">
                    <a :href="article.link" class="none">
                        <div class="card-body">
                            <h5 class="card-title text-left">{{article.title}}</h5>
                            <h6 class="card-subtitle mb-2 text-muted text-left">Published : {{article.pubDate}}</h6>
                            <div v-html="article.content"></div>
                        </div>
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Article",
        props: ["article"],

    }
</script>

<style>
    figure img{
        width: 100%;
        max-width: 900px;
        height: auto;
        max-height: 300px;
    }
    p{
        display: none;
    }
    .card-title{
        font-weight: bold;
        font-size: 30px;
    }
</style>
<style scoped>
    .none{
        text-decoration: none;
        color: #141E30;
    }
</style>