<template>
    <header>
        <nav class="navbar light" v-if="light">
            <div class="logo">
                <nuxt-link to="/">
                    <img src="~/assets/img/logo-white.png" alt="ontop builders logo" />
                </nuxt-link>
            </div>
            <div class="menu">
                <ul>
                    <li v-for="(item, index) in items" :key="index">
                        <nuxt-link :to="item.url">{{item.menu}}</nuxt-link>
                    </li>
                    <li><nuxt-link to="/contact-us" class="_cta">Contact Us</nuxt-link></li>
                </ul>
            </div>
        </nav>

        <nav class="navbar" v-else>
            <div class="logo">
                <nuxt-link to="/">
                    <img src="~/assets/img/logo.png" alt="ontop builders logo" />
                </nuxt-link>
            </div>
            <div class="menu">
                <ul>
                    <li v-for="(item, index) in items" :key="index">
                        <nuxt-link :to="item.url">{{item.menu}}</nuxt-link>
                    </li>
                    <li>
                        <nuxt-link to="/contact-us" class="_cta">Contact Us</nuxt-link>
                    </li>
                </ul>
            </div>
        </nav>
    </header>
</template>

<script>
export default {
    name: "Header",
    props: ['light'],
    data() {
        return {
            items: [
                {'id': 0, 'menu': 'Portfolio', 'url': '/portfolio'},
                {'id': 1, 'menu': 'About Us', 'url': '/about-us'},
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
header {
    position: relative;
    z-index: 99;
}

.navbar {
    width: 90%;
    max-width: 100%;
    padding: 2rem 0.9rem 1rem;
    margin: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
}


.menu {
    ul {
        display: flex;

        li {
            a {
                font-family: "Gilroy Medium", sans-serif;
                text-transform: capitalize;
                padding: 0 15px;
            }

            ._cta {
                color: $ot-red;
                padding: 12px 24px;
                margin-left: 15px;
                background-color: transparent;
                border: 1px solid $ot-red;
                box-sizing: border-box;
                border-radius: 4px;

                &:hover {
                    background-color: $ot-red;
                    color: $ot-white;
                    border: 1px solid $ot-red;
                }
            }
        }
    }
}

.light {
    .menu {
        a {
            color: $ot-white;
        }

        ._cta {
            background-color: $ot-white;
            border: 1px solid $ot-white;
        }
    }
}
</style>