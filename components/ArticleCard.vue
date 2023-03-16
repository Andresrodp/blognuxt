<template>
    <div class="article-card">
        <h3>{{ title }}</h3>
        <p>Por: {{ author }}</p>
        <p>{{ description }}</p>
        <figure>
            <img :src="image" alt="Imagen del articulo">
        </figure>
        <p>fecha: {{ date }}</p>
        <a :href="slug">Ver Artículo</a>
    </div>
</template>

<script>
    export default {
        name: 'ArticleCard',
        props: {
            title: {
                type: String,
                default: ''
            },
            author:{
                type: String,
                default: ''
            },
            description:{
                type: String,
                default: ''
            },
            image:{
                type: String,
                default: ''
            },
            date:{
                type: Date,
                default: new Date().toLocaleDateString()
            },
            slug:{
                type: String,
                default: ''
            }
        }
    }
</script>

<style>
    .article-card{
        border: 1px solid red;
        width: 30%;
        height: 30%;
        margin: 1rem;
    }
</style>