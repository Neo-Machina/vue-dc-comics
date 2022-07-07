<template>
    <footer>
        <!-- footer-top -->
        <div class="footer_top container">
            <div class="row">
                <div class="col">
                    <h3>{{ dcComics.title }}</h3>
                    
                    <ul>
                        <li v-for="(link,index) in dcComics.footerLinks" :key="index">
                            <a :href="dcComics.url">
                                {{ link }}
                            </a>
                        </li>
                    </ul>

                    <h3>{{ shop.title }}</h3>

                    <ul>
                        <li v-for="(link,index) in shop.footerLinks" :key="index">
                            <a :href="shop.url">
                                {{ link }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="col">
                    <h3>{{ dc.title }}</h3>

                    <ul>
                        <li v-for="(link,index) in dc.footerLinks" :key="index">
                            <a :href="dc.url">
                                {{ link }}
                            </a>
                        </li>                     
                    </ul>
                </div>
                <div class="col">
                    <h3>{{ sites.title }}</h3>

                    <ul>
                        <li v-for="(link,index) in sites.footerLinks" :key="index">
                            <a :href="sites.url">
                                 {{ link }}
                            </a>
                        </li>
                    </ul>
                </div>
            </div>

            <div class="dc_logo_bg">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
        <!-- footer-bottom -->
        <div class="footer_bottom">
            <div class="container">
                <button class="btn_footer">sign-up now!</button>

                <div class="flex-icon_links">
                    <h3>follows us</h3>

                    <ul>
                        <li v-for="(icon,index) in iconMenuFooter" :key="index">
                            <a href="#">
                                <img :src="icon.iconImg" :alt="icon.alt">
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'PageFooter',
    data() {
        return {
            dcComics: {
                title: 'dc comics',
                url: '#',
                footerLinks: [
                    'characters',
                    'comics',
                    'movies',
                    'tv',
                    'game',
                    'videos',
                    'news'
                ]
            },
            shop: {
                title: 'shop',
                url: '#',
                footerLinks: [
                    'shop DC',
                    'shop DC collectibles',
                ]
            },
            dc: {
                title: 'dc',
                url: '#',
                footerLinks: [
                    'terms of use',
                    'privacy police (new)',
                    'ad choices',
                    'advertising',
                    'jobs',
                    'subscriptions',
                    'talent workshops',
                    'cpsc certificates',
                    'ratings',
                    'shop help',
                    'contact us'
                ]
            },
            sites: {
                title: 'sites',
                url: '#',
                footerLinks: [
                    'DC',
                    'MAD magazine',
                    'DC kids',
                    'DC universe',
                    'DC power visa',
                ]
            },
            iconMenuFooter: [
                {
                    url: '#',
                    iconImg: require('../assets/img/footer-facebook.png'),
                    alt: 'facebook-icon'
                },
                {
                    url: '#',
                    iconImg: require('../assets/img/footer-twitter.png'),
                    alt: 'twitter-icon'
                },
                {
                    url: '#',
                    iconImg: require('../assets/img/footer-youtube.png'),
                    alt: 'youtube-icon'
                },
                {
                    url: '#',
                    iconImg: require('../assets/img/footer-pinterest.png'),
                    alt: 'pinterest-icon'
                },
                {
                    url: '#',
                    iconImg: require('../assets/img/footer-periscope.png'),
                    alt: 'periscope-icon'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables';

footer {
    height: 280px;
    background-image: url(../assets/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;

    // FOOTER-TOP
    .footer_top {
        display: flex;
        height: 100%;
        justify-content: space-between;
        
        .row {
            color: white;
            display: flex; 
            width: 350px;
            margin-top: 20px;         

            .col {
                width: calc(100% / 3);

                &:not(:last-child) {
                    padding-right: 20px;
                }

                h3 {
                        text-transform: $text_uppercase;
                        font-size: 14px;
                        padding: 12px 0;
                    }

                ul {
                    li {
                        line-height: 13px;

                        a {
                            color: $secondary_color;
                            text-transform: $text_capitalize;
                            font-size: 10px;
                        }
                    }
                }
            }
        }

        .dc_logo_bg {
            width: 27rem;
            overflow: hidden;
            margin-top: -75px;
        }
    }

    // FOOTER-BOTTOM
    .footer_bottom {
        background-color: #303030;
        height: 80px;

        .container {
            display: flex;
            height: 100%;
            align-items: center;
            justify-content: space-between;

            .btn_footer {
                color: white;
                border: 1px solid $brand_main_color;
                padding: 10px;
                background-color: #303030;
                text-transform: $text_uppercase;
                cursor: pointer;
            }

            .flex-icon_links {
                display: flex;
                align-items: center;

                h3 {
                    text-transform: $text_uppercase;  
                    font-size: 15px;     
                    margin-right: 15px;
                    color: $brand_main_color;
                }

                ul {
                    li {
                        display: inline-block;
                        margin: 0 8px;

                        a {
                            img {
                                width: 28px;
                            }
                        }
                    }
                }
            }
        }
    }
}
</style>