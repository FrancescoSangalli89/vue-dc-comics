<template>
    <footer>
        <div class="footerTop">
            <nav>
                <ul class="HeaderMenu">
                    <li v-for="(link, index) in links" :key="index" >
                        <img :src="link.icon" />
                        <a :href="link.url" :class="link.active?'active':''" >{{link.text}}</a>
                    </li>
                </ul>
            </nav>
        </div>
        <div class="footerBtm">

        </div>
    </footer>
</template>

<script>
export default {
    name: 'MyFooter',
    data() {
        return {
            links: [
                {
                    text: 'DIGITAL COMICS',
                    url: '#',
                    icon: '@/assets/images/buy-comics-digital-comics.png',
                    active: false
                },
                {
                    text: 'DC MERCHANDISE',
                    url: '#',
                    icon: '@/assets/images/buy-comics-merchandise.png',
                    active: false
                },
                {
                    text: 'SUBSCRIPTION',
                    url: '#',
                    icon: '@/assets/images/buy-comics-subscriptions.png',
                    active: false
                },
                {
                    text: 'COMIC SHOP LOCATOR',
                    url: '#',
                    icon: '@/assets/images/buy-comics-shop-locator.png',
                    active: false
                },
                {
                    text: 'DC POWER VISA',
                    url: '#',
                    icon: '@/assets/images/buy-dc-power-visa',
                    active: false
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">

    @import '../styles/vars.scss'; 

    .footerTop {
        background-color: $brand-color;
        height: 155px;
        display: flex;
        justify-content: center;
        align-items: center;

        nav {


            ul {
                display: flex;
                list-style: none;
                justify-content: center;
                align-items: center;

                li {
                    padding: 0 10px;
                    font-weight: 600;
                    line-height: 115px;

                    a {
                        text-decoration: none;
                        color: #fff;
                        display: inline-block;
                    }
                }
            }
        }
    }
</style>