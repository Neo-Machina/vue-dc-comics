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
    background-color: pink;
    height: 90px;

    .flex-header {
    display: flex;
    justify-content: space-between;
    height: 100%;
    align-items: center;
    }

    .logo {
        img {
            width: 60px;
        }
    }

    nav {
        ul {
            display: flex;

            li {
                padding: 0 10px;

                &.selected-item {
                    display: inline-block;
                    line-height: 0.9;
                    border-bottom: 4px solid $brand_main_color;      
                }

                a {
                    font-size: 10px;
                    text-transform: uppercase;
                }
            }
        }
    }
}
</style>