<template>
    <header>
        <div class="container flex-header">
            <!-- header-logo -->
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="logo-dc">
            </div>

            <!-- header-nav -->
            <nav>
                <ul>
                    <li v-for="(link, index) in menuLinks" :key="index" :class="{ 'selected-item' : link.current }">
                        <a :href="url">
                            {{ link.text }}
                        </a>
                    </li>          
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
    name: 'PageHeader',
    data() {
        return {
            menuLinks: [
                {
                    text: 'characters',
                    url: '#',
                    current: false
                },
                {
                    text: 'comics',
                    url: '#',
                    current: true
                },
                {
                    text: 'movies',
                    url: '#',
                    current: false
                },
                {
                    text: 'tv',
                    url: '#',
                    current: false
                },
                {
                    text: 'games',
                    url: '#',
                    current: false
                },
                {
                    text: 'collectibles',
                    url: '#',
                    current: false
                },
                {
                    text: 'videos',
                    url: '#',
                    current: false
                },
                {
                    text: 'fans',
                    url: '#',
                    current: false
                },
                {
                    text: 'news',
                    url: '#',
                    current: false
                },
                {
                    text: 'shop',
                    url: '#',
                    current: false
                }
        ]   
        }
    } 
}
</script>

<style lang="scss" scoped>
@import '../style/variables';

header {
    height: 90px;

    .flex-header {
    display: flex;
    justify-content: space-between;
    height: 100%;
    align-items: center;
    }
    // logo
    .logo {
        img {
            width: 60px;
        }
    }
    // nav
    nav {
        height: 100%;

        ul {
            height: 100%;
            display: flex;

            li {
                padding: 0 10px;
                position: relative;
                line-height: 90px;
                cursor: pointer;

                &.selected-item {
                    color: $brand_main_color;

                    &::after {
                        content: "";
                        height: 3px;
                        width: 100%;
                        position: absolute;
                        bottom: 0;
                        left: 0;
                        display: inline-block;
                        background-color: $brand_main_color;
                    }
                    
                }

                a {
                    font-size: 10px;
                    text-transform: $text_uppercase;
                }
            }
        }
    }
}
</style>