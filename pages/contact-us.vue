<template>
    <div>
        <section class="hero">
            <div class="_inner ot-container">
                <div class="text">
                    <h4>Have a project?</h4>
                    <h1>Contact us</h1>
                </div>

                <div class="img">
                    <img src="~/assets/img/happy-ontop-builders-staff.png" alt="About OT" />
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
</style>