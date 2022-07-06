<template>
    <footer>
        <!-- footer-top -->
        <div class="footer_top container">
            <div class="row">
                <div class="col">
                    <h3>{{ dcComics.title }}</h3>
                    
                    <ul>
                        <li v-for="(link,index) in dcComics.footerLinks" :key="index">
                            <a href="#">
                                {{ link }}
                            </a>
                        </li>
                    </ul>

                    <h3>{{ shop.title }}</h3>

                    <ul>
                        <li v-for="(link,index) in shop.footerLinks" :key="index">
                            <a href="#">
                                {{ link }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="col">
                    <h3>{{ dc.title }}</h3>

                    <ul>
                        <li v-for="(link,index) in dc.footerLinks" :key="index">
                            <a href="#">
                                {{ link }}
                            </a>
                        </li>                     
                    </ul>
                </div>
                <div class="col">
                    <h3>{{ sites.title }}</h3>

                    <ul>
                        <li v-for="(link,index) in sites.footerLinks" :key="index">
                            <a href="#">
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
        <div>

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
                footerLinks: [
                    'shop DC',
                    'shop DC collectibles',
                ]
            },
            dc: {
                title: 'dc',
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
                footerLinks: [
                    'DC',
                    'MAD magazine',
                    'DC kids',
                    'DC universe',
                    'DC power visa',
                ]
            }
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
}
</style>