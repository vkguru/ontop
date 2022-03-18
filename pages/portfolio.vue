<template>
    <div>
        <section class="hero">
            <div class="_inner">
                <div class="text">
                    <h4>Our works</h4>
                    <h1>Portfolio</h1>
                    <p>We pride ourselves in the delivery of industry standard projects. We follow international best practices to make this happen.</p>
                </div>

                <div class="img">
                    <img src="~/assets/img/portfolio-client.png" alt="Ontop staff on a project" />
                    <div class="_info">
                        <span>
                            <h4>20+</h4>
                            <p>Clients projects</p>
                        </span>
                        <img src="~/assets/img/radial.png" />
                    </div>
                </div>
            </div>
        </section>

        <section>
            <div class="ot-container">
                <PortfolioCard
                    :title="`Building construction`"
                    :location="`Gbagada`"
                    :description="`Lorem ipsum dolor sit amet, consectetur adipiscing elit. Facilisi habitasse sit volutpat sit massa erat. Aliquam felis dui, est id. Cursus orci magna in lectus mi consectetur eros tellus. Ante orci sed nibh vel scelerisque lacus, elit id.`"
                    :images="gbagada"
                />
            </div>
        </section>

        <section>
            <div class="ot-container">
                <PortfolioCard
                    :title="`Building construction`"
                    :location="`Osborne offshore estate`"
                    :description="`Lorem ipsum dolor sit amet, consectetur adipiscing elit. Facilisi habitasse sit volutpat sit massa erat. Aliquam felis dui, est id. Cursus orci magna in lectus mi consectetur eros tellus. Ante orci sed nibh vel scelerisque lacus, elit id.`"
                    :images="osborne"
                />
            </div>
        </section>

        <section>
            <div class="ot-container">
                <PortfolioCard
                    :title="`Multi purpose hall`"
                    :location="`Maryland Catholic secondary school`"
                    :description="`Lorem ipsum dolor sit amet, consectetur adipiscing elit. Facilisi habitasse sit volutpat sit massa erat. Aliquam felis dui, est id. Cursus orci magna in lectus mi consectetur eros tellus. Ante orci sed nibh vel scelerisque lacus, elit id.`"
                    :images="maryland"
                />
            </div>
        </section>

        <section>
            <div class="ot-container">
                <PortfolioCard
                    :title="`Building construction`"
                    :location="`Magboro`"
                    :description="`Lorem ipsum dolor sit amet, consectetur adipiscing elit. Facilisi habitasse sit volutpat sit massa erat. Aliquam felis dui, est id. Cursus orci magna in lectus mi consectetur eros tellus. Ante orci sed nibh vel scelerisque lacus, elit id.`"
                    :images="magboro"
                />
            </div>
        </section>

        <section>
            <div class="ot-container">
                <PortfolioCard
                    :title="`Supermarket building`"
                    :location="`Prince Ebeano supermarket`"
                    :description="`Lorem ipsum dolor sit amet, consectetur adipiscing elit. Facilisi habitasse sit volutpat sit massa erat. Aliquam felis dui, est id. Cursus orci magna in lectus mi consectetur eros tellus. Ante orci sed nibh vel scelerisque lacus, elit id.`"
                    :images="ebeano"
                />
            </div>
        </section>

        <section>
            <PreFooter />
        </section>
    </div>
</template>

<script>
export default {
    data() {
        return {
            gbagada: [
                'gb-one.jpg',
                'gb-two.jpg',
                'gb-three.jpg',
                'gb-four.jpg',
            ],
            osborne: [
                'os-one.jpg',
                'os-two.jpg',
                'os-three.jpg',
                'os-four.jpg',
            ],
            maryland: [
                'mp-one.jpg',
                'mp-two.jpg',
                'mp-three.jpg',
                'mp-four.jpg',
            ],
            magboro: [
                'mg-one.jpg',
                'mg-two.jpg',
                'mg-three.jpg',
                'mg-four.jpg',
            ],
            ebeano: [
                'pe-one.jpg',
                'pe-two.jpg',
                'pe-three.jpg',
                'pe-four.jpg',
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
section {
    margin: 100px 0;
}

.hero {
    padding: 12rem 0;
    margin-top: -100px;
    margin-bottom: 100px;
    background-color: #fff7f7;

    ._inner {
        display: flex;
        justify-content: space-between;
        width: 94%;
        margin-left: auto;

        & .text {
            max-width: 400px;

            & h4 {
                font-size: 24px;
                font-family: "Aeonik TRIAL";
                font-weight: 400;
                opacity: 0.5;
                padding-bottom: 30px;
            }

            & h1 {
                font-size: 3.813rem;
                font-family: 'Aeonik TRIAL';
                font-weight: 400;
                padding-bottom: 30px;
            }
        }

        & .img {
            position: relative;

            & ._info {
                display: flex;
                align-items: center;
                position: absolute;
                left: -187px;
                bottom: -203px;

                & span {
                    background-color: $ot-white;
                    position: relative;
                    left: 114px;
                    bottom: 0;
                    padding: 20px;
                    text-align: center;
                    width: 230px;
                    border-radius: 24px;
                    box-shadow: 0px 14px 24px 20px rgba(0, 0, 0, 0.04);
                    z-index: 2;

                    & h4 {
                        font-size: 24px;
                    }

                    & p {
                        font-size: 14px;
                    }
                }

                & img {
                    position: relative;
                    top: -35px;
                }
            }
        }
    }
}

@media screen and (max-width: 900px) {
    .hero {
        ._inner {
            flex-direction: column;
            width: 90%;
            margin-right: auto;

            .text {
                max-width: 100%;
                margin-bottom: 30px;
            }

            .img {
                width: 100%;

                img {
                    width: 100%;
                    border-radius: 60px;
                }

                ._info {
                    left: -35px;
                    bottom: -150px;
                    width: 250px;
                }
            }
        }
    }
}
</style>