<template>
    <header>
        <div class="container">
            <div class="LogoContainer">
                <img class="DcLogo" src="@/assets/images/dc-logo.png" alt="dc logo">
            </div>
            <nav>
                <ul class="HeaderMenu">
                    <li v-for="(link, index) in links" :key="index" >
                        <a :href="link.url" :class="link.active?'active':''" >{{link.text}}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
    name: 'MyHeader',
    data() {
        return {
            links: [
                {
                    text: 'CHARACTERS',
                    url: '#',
                    active: false
                },
                {
                    text: 'COMICS',
                    url: '#',
                    active: true
                },
                {
                    text: 'MOVIES',
                    url: '#',
                    active: false
                },
                {
                    text: 'TV',
                    url: '#',
                    active: false
                },
                {
                    text: 'GAMES',
                    url: '#',
                    active: false
                },
                {
                    text: 'COLLECTIBLES',
                    url: '#',
                    active: false
                },
                {
                    text: 'VIDEOS',
                    url: '#',
                    active: false
                },
                {
                    text: 'FAN',
                    url: '#',
                    active: false
                },
                {
                    text: 'NEW',
                    url: '#',
                    active: false
                },
                {
                    text: 'SHOP',
                    url: '#',
                    active: false
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">

    @import '../styles/vars.scss';
    @import '../styles/utilities.scss';

    * {
        height: 100%;
    }

    header {
        height: 115px;

        .container {

            display: flex;
            align-items: center;
            justify-content: space-between;
            
            .LogoContainer {
                height: 100%;
                display: flex;
                align-items: center;

            .DcLogo {
                    height: 80px;
                }
            }

            .HeaderMenu {
                display: flex;
                list-style: none;

                li {
                    padding: 0 10px;
                    font-weight: 600;
                    line-height: 115px;

                    a {
                        text-decoration: none;
                        color: black;
                        display: inline-block;

                        &.active, &:hover {
                        color: $brand-color;
                        border-bottom: 8px solid $brand-color;
                    }

                    }
                }
            }

        }
    }
</style>