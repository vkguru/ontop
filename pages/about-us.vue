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

        <section id="deliver">
            <div class="_inner">
                <h2>Yes, <span>We deliver</span></h2>
                <p>We are an emerging firm armed with state of the art equipment, 21st century expertise coupled with a high level of intellectual compatibility and tactically proficiency. We possess a deep sense of commitment and first class customer orientation nationally and internationally.</p>
            </div>
        </section>

        <section id="team">
            <div class="ot-container">
                <header>
                    <h2>Our Team</h2>
                    <p>The strength of this company is in its ability to bring together more than 20 active individual professionals in construction industry; to understand client needs and offer proactive technical services that ensures quality delivery</p>
                </header>
                <div class="_row">
                    <TeamCard
                        :imageName="`Olusola-Matthew.jpg`"
                        :staffName="`Olusola Matthew Orikoku`"
                        :qualification="`OND, HND, PGD, MNIOB, CORBON, ANIM, Masters in Project Management`"
                        :position="`Managing Director`"
                    />

                    <TeamCard
                        :imageName="`Engr-Abraham-Olaolu.jpg`"
                        :staffName="`Engr Abraham Olaolu Orikoku`"
                        :qualification="`Bsc Civil Engr, COREN`"
                        :position="`HSE Engineer`"
                    />

                    <TeamCard
                        :imageName="`Orikoku-Opemipo.jpg`"
                        :staffName="`Orikoku Opemipo Ebunola`"
                        :qualification="`BSc. Accounting, MBA, ACA, ACCA, MSC (In view)`"
                        :position="`Personnel & Internal Control Manager`"
                    />

                    <TeamCard
                        :imageName="`Fajimi-Kayode-Paul.jpg`"
                        :staffName="`Fajimi Kayode Paul`"
                        :qualification="`Bsc Elect. Eng, MNSE, COREN`"
                        :position="`Electrical Engr`"
                    />
                </div>

                <div class="_row">
                    <TeamCard
                        :imageName="`Oguntola-Lateef-A.jpg`"
                        :staffName="`Oguntola Lateef A`"
                        :qualification="`OND (Building), Bsc (civil), COREN, NIStructE`"
                        :position="`Structural Engineer`"
                    />

                    <TeamCard
                        :imageName="`default.jpg`"
                        :staffName="`Awoyinfa Titilayo`"
                        :qualification="`Bsc Architecture (NIA, ARCON)`"
                        :position="`Chief Architect`"
                    />

                    <TeamCard
                        :imageName="`default.jpg`"
                        :staffName="`Omosalewa Olukunga`"
                        :qualification="`OND, HND, BTech Architecture`"
                        :position="`Architect 1`"
                    />

                    <TeamCard
                        :imageName="`default.jpg`"
                        :staffName="`Omosalewa Olukunga`"
                        :qualification="`OND, HND, BTech Architecture`"
                        :position="`Architect 1`"
                    />
                </div>
            </div>
        </section>

        <section id="affiliates">
            <div class="ot-container">
                <header>
                    <h2>Professional bodies affiliation</h2>
                    <p>The firm and or staff maintain regular and current subscriptions with the following professional bodies:</p>
                </header>
                <img src="~/assets/img/ontop-affiliations.png" />
            </div>
        </section>

        <section id="equip">
            <div class="ot-container">
                <header>
                    <h2>Plants and Equipments</h2>
                    <p>We utilize computers extensively with the support of the following hardware and equipment:</p>
                </header>
                <div class="_row">
                    <EquipCard 
                        :equipImg="`Garmin-GPSIII.png`"
                        :equipName="`Garmin GPSIII Global Positioning System Device`"
                    />

                    <EquipCard 
                        :equipImg="`Wild-TC800.png`"
                        :equipName="`Wild TC800 Total Station Surveying Instrument`"
                    />

                    <EquipCard 
                        :equipImg="`Wild-12.png`"
                        :equipName="`Wild T2 Theodolite`"
                    />
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

#deliver {
    background-image: url('../assets/img/deliver.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    color: #fff;
    padding: 150px 100px;
    margin-top: 100px;
    height: 600px;

    & ._inner {
        max-width: 693px;
        transform: translateY(50px);

        & h2 {
            font-size: 60px;
            font-family: "Aeonik TRIAL";
            font-weight: 400;
            margin-bottom: 50px;

            & span {
                font-family: "Aeonik TRIAL Bold";
            }
        }

        & p {
            font-size: 18px;
            line-height: 36px;
        }
    }
}

#team {
    margin: 150px 0;

    & header {
        max-width: 670px;
        margin: auto;
        text-align: center;

        & h2 {
            font-family: 'Aeonik TRIAL';
            font-weight: 400;
            font-size: 30px;
            padding-bottom: 16px;
        }
    }

    & ._row {
        display: flex;
        column-gap: 30px;
        justify-content: space-between;
        margin: 100px auto;
        max-width: 1200px;
    }
}

#affiliates {
    margin: 150px 0;

    & header {
        max-width: 670px;
        margin: auto;
        text-align: center;

        & h2 {
            font-family: 'Aeonik TRIAL';
            font-weight: 400;
            font-size: 30px;
            padding-bottom: 16px;
        }
    }

    & img {
        margin-top: 60px;
        width: 100%;
    }
}

#equip {
    margin: 150px 0;

    & header {
        max-width: 670px;
        margin: auto;
        text-align: center;

        & h2 {
            font-family: 'Aeonik TRIAL';
            font-weight: 400;
            font-size: 30px;
            padding-bottom: 16px;
        }
    }

    & ._row {
        display: flex;
        column-gap: 30px;
        justify-content: space-between;
        margin: 100px auto;
        max-width: 1200px;
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

@media screen and (max-width: 1108px) and (min-width: 600px) {
    #team ._row {
        flex-wrap: wrap;
    }
}


@media screen and (max-width: 600px) {
    .hero #radia {
        display: none;
    }

    #team ._row {
        flex-direction: column;
    }

    #equip ._row {
        flex-direction: column;
    }

    #deliver {
        padding: 150px 50px;
        height: auto;
    }

    #deliver ._inner h2 {
        line-height: 70px;
    }
}

</style>