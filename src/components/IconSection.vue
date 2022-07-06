<template>
    <section>
        <div class="container">
            <ul>
                <li v-for="(icon, index) in iconMenu" :key="index">
                    <a :href="icon.url" >
                        <div class="flex-link">
                            <img :src="icon.imgSrc" :altImg="icon.alt">

                            <div>{{ icon.text }}</div>
                        </div>
                    </a>
                </li>
                
            </ul>
        </div>
    </section>
</template>

<script>
export default {
    name:'IconSection',
    data() {
        return {
            iconMenu: [
                {
                    url: '#',
                    imgSrc: require('../assets/img/buy-comics-digital-comics.png'),
                    altImg: 'digital-comics',
                    text: 'digital comics'
                },
                {
                    url: '#',
                    imgSrc: require('../assets/img/buy-comics-merchandise.png'),
                    altImg: 'dc merchandise',
                    text: 'dc merchandise'
                },
                {
                    url: '#',
                    imgSrc: require('../assets/img/buy-comics-subscriptions.png'),
                    altImg: '../assets/img/subscription',
                    text: 'subscription'
                },
                {
                    url: '#',
                    imgSrc: require('../assets/img/buy-comics-shop-locator.png'),
                    altImg: 'comic shop locator',
                    text: 'comic shop locator'
                },
                {
                    url: '#',
                    imgSrc: require('../assets/img/buy-dc-power-visa.svg'),
                    altImg: 'visa',
                    text: 'dc power visa'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables';

section {
    height: 110px;
    background-color: $brand_main_color;
    position: relative;

    .container {
        height: 100%;
        z-index: 10;
        ul {
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: space-around;

            li {
                a {
                    .flex-link {
                        display: flex;
                        align-items: center;

                        img {
                            width: 35px;
                            margin-right: 12px;
                        }

                        div {
                            font-size: 11px;
                            text-transform: $text_uppercase;
                            color: white;
                        }
                    }
                }
            }
        }
    }
}



</style>