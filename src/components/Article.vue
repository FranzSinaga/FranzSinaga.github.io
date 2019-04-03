<template>
    <div style="background-color: azure">
        <div class="canhide container">
            <div class="card">
                <div class="card-heading">{{article.title}}</div>
                <div class="card-body" v-html=" article.description"></div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Article",
        props: ["article"]
    }
</script>

<style scoped>

</style>