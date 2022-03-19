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
            <div class="hamburger" @click="reveal">
                <span></span>
                <span></span>
                <span></span>
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
            <div class="hamburger" @click="reveal">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </nav>

        <div class="mobile-menu" v-if="showMenu">
            <nav class="navbar light">
                <div class="logo">
                    <nuxt-link to="/">
                        <img src="~/assets/img/logo-white.png" alt="ontop builders logo" />
                    </nuxt-link>
                </div>
                <div class="hamburger-open" @click="reveal">
                    <span></span>
                    <span></span>
                </div>
            </nav>
            <div class="menu-list">
                <ul>
                    <li v-for="(item, index) in items" :key="index" @click="reveal">
                        <nuxt-link :to="item.url">{{item.menu}}</nuxt-link>
                    </li>
                    <li @click="reveal"><nuxt-link to="/contact-us">Contact Us</nuxt-link></li>
                </ul>
            </div>
        </div>
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
            ],
            showMenu: false
        }
    },
    methods: {
        reveal() {
            this.showMenu = !this.showMenu;
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

.hamburger {
    width: 25px;
    height: 25px;
    cursor: pointer;
    display: none;

    & span {
        background-color: $ot-black;
        height: 2px;
        width: 100%;
        margin-bottom: 5px;
        display: block;

        &:nth-child(1) {
            width: 30%;
        }

        &:nth-child(2) {
            width: 80%;
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

    .hamburger {
        & span {
            background-color: $ot-white;
        }
    }

    .hamburger-open {
        width: 25px;
        cursor: pointer;

        & span {
            background-color: $ot-white;
            height: 2px;
            width: 100%;
            margin-bottom: 5px;
            display: block;

            &:nth-child(1) {
                transform: rotate(135deg);
            }

            &:nth-child(2) {
                transform: rotate(-135deg);
                margin-top: -7px;
            }
        }
    }
}

.mobile-menu {
    position: fixed;
    top: 0;
    background-color: #333;
    height: 100%;
    width: 100%;
}

.menu-list {
    width: 90%;
    padding: 2rem 0.9rem 1rem;
    margin: auto;
    
    & ul {
        & li { 
            padding-bottom: 20px;
            
            & a {
                color: $ot-white;
            }
        }
    }
}

@media screen and (max-width: 768px) {
    .menu {
        display: none;
    }

    .hamburger {
        display: block;
    }
}
</style>