<template>
    <footer>
        <div class="ft">
            <div class="ft-brand">
                <img src="~/assets/img/logo-white.png" alt="ontop builders logo" />
                <p>We deliver projects that defies all limitations</p>
            </div>
            <div class="ft-info">
                <div class="_link">
                    <ul>
                        <li v-for="(item, index) in items" :key="index">
                            <router-link :to="item.url">{{item.menu}}</router-link>
                        </li>
                    </ul>
                </div>
                <div class="_details">
                    <div class="col">
                        <h4>Office Address:</h4>
                        <p>Suite 29 LSDPC office complex phase 3, oba ogunji road, ogba ikeja. Lagos</p>
                    </div>

                    <div class="col">
                        <h4>Contact:</h4>
                        <a href="tel:+2348032836675">+234 803 283 6675</a>
                    </div>

                    <div class="col">
                        <h4>Email:</h4>
                        <a href="mailto:ontopbuilders@gmail.com">ontopbuilders@gmail.com</a>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: "Footer",
    data() {
        return {
            items: [
                {'id': 0, 'menu': 'Our Services', 'url': '/#service'},
                {'id': 1, 'menu': 'Portfolio', 'url': '/portfolio'},
                {'id': 2, 'menu': 'About Us', 'url': '/about-us'},
                {'id': 3, 'menu': 'Contact Us', 'url': '/contact-us'},
                {'id': 4, 'menu': 'Policies', 'url': '/policies'},
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
footer {
    width: 100%;
    background-color: $ot-black;
}

.ft {
    display: flex;
    justify-content: space-between;
    width: 90%;
    margin: auto;
    padding: 3rem 0.9rem 6rem;
    color: $ot-white;
    column-gap: 253px;
}

.ft-brand {
    p {
        padding-right: 30px;
        padding-top: 19px;
    }
}

.ft-info {
    display: flex;
    flex-direction: column;

    ._link {
        max-width: 608px;

        @media screen and (max-width: 768px) {
            margin-top: 30px;
        }
        ul {
            display: flex;
            justify-content: space-between;
            li {

                a {
                    color: $ot-white;
                }
            }
        }
    }

    ._details {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-column-gap: 1.5rem;
        margin-top: 53px;

        @media screen and (max-width: 600px) {
            grid-template-columns: repeat(1, 1fr);
        }

        .col {
            padding-right: 80px;

            @media screen and (max-width: 768px) {
                padding-right: 0;
            }

            @media screen and (max-width: 600px) {
                margin-bottom: 20px;
            }

            h4 {
                font-family: "Gilroy Medium", sans-serif;
                font-weight: 500;
                padding-bottom: 15px;
            }

            a {
                color: $ot-white;
            }
        }
    }
}

@media screen and (max-width: 1380px) and (min-width: 769px)  {
    .ft {
        column-gap: 50px;
    }

    .ft-info ._details .col {
        padding-right: 0;
    }
}

@media screen and (max-width: 768px) {
    .ft {
        flex-direction: column;
    }
}

@media screen and (max-width: 600px) {
    .ft-info ._link ul {
        justify-content: start;
        flex-wrap: wrap;
        column-gap: 10px;
    }
}

</style>