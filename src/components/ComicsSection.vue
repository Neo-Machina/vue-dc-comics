<template>
    <section>
        <img src="../assets/img/jumbotron.jpg" alt="jumbotron">

        <div class="container">
            <div class="current_series">current series</div>

            <div class="row">
                <ComicCard v-for="(element,index) in comics" :key="index" :cardDetailes="element" />
            </div>

            <button class="button_comics">load more</button>
        </div>
    </section>
</template>

<script>
import ComicCard from "./ComicCard.vue";
import DcComicsJson from "../assets/dc-comics.json";

export default {
    name: 'ComicsSection',
    components: {
        ComicCard,
    },
    data() {
        return {
            comics: DcComicsJson
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables';

section {
    color: white;
    height: 52.5rem;
    background-color: #1c1c1c;

    img {
        height: 19.8rem;
        object-fit: cover;
        object-position: center 0px;
    }

    .container {
        position: relative; 

        .current_series {
            background-color: $brand_main_color;
            padding: 10px 20px;
            display: inline-block;
            text-transform: $text_uppercase;
            font-size: 18px;
            font-weight: bold;
            position: absolute;
            top: -22px;
        }

        .row {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
        } 

        .button_comics {
            text-transform: uppercase;
            padding: 10px 50px;
            background-color: $brand_main_color;
            font-size: 11px;
            color: white;
            border: $brand_main_color;
            position: absolute;
            top: 490px;
            left: 50%;
            -ms-transform: translate(-50%, -50%);
            transform: translate(-50%, -50%);
        }
    } 
}
</style>