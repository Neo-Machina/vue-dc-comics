<template>
    <div class="col">
        <div class="comic_card">
            <img :src="cardDetailes.thumb" :alt="cardDetailes.series">

            <h3>{{ cardDetailes.series }}</h3>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ComicCard',
    props: {
        cardDetailes: Object
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables';

.row {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    margin: 0 15px;

    .col {
        width: calc((100% / 6) - 20px);

        .comic_card {
            margin-top: 40px;

            img {
                aspect-ratio: 1/1;
                object-fit: cover;
                object-position: center 0;
            }

            h3 {
                text-transform: $text_uppercase;
                font-size: 10px;
                margin-top: 10px;
            }
        }
    }
}
</style>