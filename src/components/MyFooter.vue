<template>
    <footer>
        <div class="footerTop">
            <nav>
                <ul class="middleMenu">
                    <li v-for="(link, index) in links" :key="index" >
                        <img :src="link.icon" />
                        <a :href="link.url" >{{link.text}}</a>
                    </li>
                </ul>
            </nav>
        </div>
        <div class="footerBtm">
            <div class="container">
                <FooterMenu :title="'DC COMICS'" :urls="dcComicsLinks" />
                <FooterMenu :title="'SHOP'" :urls="shopLinks" />
                <FooterMenu :title="'DC'" :urls="dcLinks" />
                <FooterMenu :title="'SITES'" :urls="siteLinks" />
                <img src="../assets/images/dc-logo-bg.png" alt="dc footer logo" />
            </div>
        </div>
        <div class="pageEnding">
            <div class="container">
                <button>SIGN-UP NOW!</button>
                <div class="social-icons">
                    <h4>FOLLOW US</h4>
                    <ul>
                        <li v-for="(icon, index) in icons" :key="index" >
                            <img :src="icon.icon" />
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>

import FooterMenu from './FooterMenu.vue';

export default {
    name: 'MyFooter',
    components: {
    FooterMenu
},
    data() {
        return {
            links: [
                {
                    text: 'DIGITAL COMICS',
                    url: '#',
                    icon: require('../assets/images/buy-comics-digital-comics.png'),
                    active: false
                },
                {
                    text: 'DC MERCHANDISE',
                    url: '#',
                    icon: require('@/assets/images/buy-comics-merchandise.png'),
                    active: false
                },
                {
                    text: 'SUBSCRIPTION',
                    url: '#',
                    icon: require('@/assets/images/buy-comics-subscriptions.png'),
                    active: false
                },
                {
                    text: 'COMIC SHOP LOCATOR',
                    url: '#',
                    icon: require('@/assets/images/buy-comics-shop-locator.png'),
                    active: false
                },
                {
                    text: 'DC POWER VISA',
                    url: '#',
                    icon: require('@/assets/images/buy-dc-power-visa.svg'),
                    active: false
                }
            ],
            dcComicsLinks: [
                {
                    text: 'Characters',
                    url: '#',
                },
                {
                    text: 'Comics',
                    url: '#',
                },
                {
                    text: 'Movies',
                    url: '#',
                },
                {
                    text: 'TV',
                    url: '#',
                },
                {
                    text: 'Games',
                    url: '#',
                },
                {
                    text: 'Videos',
                    url: '#',
                },
                {
                    text: 'news',
                    url: '#',
                }
            ],
            shopLinks: [
                {
                    url: '#',
                    text: 'Shop DC'
                },
                {
                    url: '#',
                    text: 'Shop DC Collectibles'
                },
            ],
            dcLinks: [
                {
                    text: 'Terms Of Use',
                    url: '#',
                },
                {
                    text: 'Privacy policy (New)',
                    url: '#',
                },
                {
                    text: 'Ad Choices',
                    url: '#',
                },
                {
                    text: 'Advertising',
                    url: '#',
                },
                {
                    text: 'Jobs',
                    url: '#',
                },
                {
                    text: 'Subscriptions',
                    url: '#',
                },
                {
                    text: 'Talent Workshops',
                    url: '#',
                },
                {
                    text: 'CPSC Certificates',
                    url: '#',
                },
                {
                    text: 'Ratings',
                    url: '#',
                },
                {
                    text: 'Shop Help',
                    url: '#',
                },
                {
                    text: 'Contact Us',
                    url: '#',
                }
            ],
            siteLinks: [
                {
                    text: 'DC',
                    url: '#',
                },
                {
                    text: 'MAD Magazine',
                    url: '#',
                },
                {
                    text: 'DC Kids',
                    url: '#',
                },
                {
                    text: 'DC Universe',
                    url: '#',
                },
                {
                    text: 'DC Power Visa',
                    url: '#',
                }
            ],
            icons: [
                {
                    icon: require('@/assets/images/footer-facebook.png')
                },
                {
                    icon: require('@/assets/images/footer-periscope.png')
                },
                {
                    icon: require('@/assets/images/footer-pinterest.png')
                },
                {
                    icon: require('@/assets/images/footer-twitter.png')
                },
                {
                    icon: require('@/assets/images/footer-youtube.png')
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

                    img {
                        height: 50px;
                        margin-right: 10px;
                        vertical-align: middle;
                    }

                    a {
                        text-decoration: none;
                        color: #fff;
                        display: inline-block;
                    }
                }
            }
        }
    }

    .footerBtm {
        height: 480px;
        background-image: url('../assets/images/footer-bg.jpg');
        padding: 2rem;
        
        .container {
            display: flex;

            img {
                height: 440px;
            }
        }
    }

    .pageEnding {
        height: 105px;
        width: 100%;
        background-color: $footer-color;
        line-height: 105px;
        
        .container {
            display: flex;
            align-items: center;
            justify-content: space-between;

            button {
                background-color: rgba($color: #fff, $alpha: 0);
                color: #fff;
                border: 2px $brand-color solid;
                padding: 1rem;
            }

            .social-icons {
                display: flex;

                h4 {
                    vertical-align: middle;
                    color: $brand-color;
                    margin-right: 1rem;
                }

                ul {
                    display: flex;
                    list-style: none;

                        img {
                            vertical-align: middle;
                            padding: 0 0.5rem;
                        }
                }
            }
        }

        
    }
</style>