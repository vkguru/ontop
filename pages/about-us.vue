<template>
    <div>
        <section class="hero">
            <div class="_inner ot-container">
                <div class="text">
                    <h4>Who we are</h4>
                    <h1>About us</h1>
                    <p><b>ONTOP BUILDERS LIMITED (RC 1742764)</b> is a construction and project management company in Nigeria, which was incorporated to carry on the business of building construction, project management, construction management and facility management, design/build of first class building and other civil engineering services, consulting and general contracting services to clients in both the public and private sectors.</p>
                </div>

                <div class="img">
                    <img src="~/assets/img/about-ot.png" alt="About OT" />
                    <div class="_info">
                        <span>
                            <h4>200+</h4>
                            <p>Collective staff experience</p>
                        </span>
                        <img src="~/assets/img/radial.png" />
                    </div>
                </div>
            </div>
            <img id="radia" src="~/assets/img/about-radial.png" />
        </section>

        <section>
            <div class="ot-container">
                <div class="re">
                    <img src="~/assets/img/mission.png" />
                    <h3>Mission</h3>
                    <p>To build a formidable and efficient company that will deliver construction projects that defies all imitation through application of an improved standard engineering practice in our world.</p>
                </div>

                <div class="re">
                    <img src="~/assets/img/vision.png" />
                    <h3>Vision</h3>
                    <p>To become a leading construction and project management company in the international community</p>
                </div>
            </div>
        </section>

        <section>
            <PreFooter />
        </section>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
.hero {
    position: relative;
    padding: 12rem 0;
    margin-top: -100px;
    margin-bottom: 100px;
    background-color: #fff7f7;

    #radia {
        position: absolute;
        top: 520px;
    }

    ._inner {
        display: flex;
        justify-content: space-between;
        width: 94%;
        margin-left: auto;

        & .text {
            max-width: 550px;

            & h4 {
                font-size: 24px;
                font-family: "Aeonik TRIAL";
                font-weight: 400;
                opacity: 0.5;
                padding-bottom: 40px;
            }

            & h1 {
                font-size: 3.813rem;
                font-family: 'Aeonik TRIAL';
                font-weight: 400;
                padding-bottom: 80px;
            }

            & p {
                font-size: 18px;
                line-height: 30px;
            }
        }

        & .img {
            position: relative;

            & ._info {
                display: flex;
                align-items: center;
                position: absolute;
                left: -43px;
                bottom: -196px;

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

.re {
    text-align: center;
    max-width: 800px;
    margin: 0 auto 80px;

    & img {
        padding-bottom: 30px;
    }

    & h3 {
        font-family: "Aeonik TRIAL";
        font-size: 36px;
        font-weight: 400;
        padding-bottom: 30px;
    }

    & p {
        font-size: 18px;
        line-height: 29px;
    }
}
</style>