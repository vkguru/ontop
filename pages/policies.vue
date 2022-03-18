<template>
    <div>
        <section class="hero">
            <div class="_inner ot-container">
                <div class="text">
                    <h4>Quality Assurance & Policies</h4>
                    <h1>Health, Safety and Environmental Policies</h1>
                </div>
            </div>
            <div class="tab-content ot-container">
                <div class="tab">
                    <ul>
                        <li v-for="(tab, index) in tabs" :key="index" @click="selectTab(index)" :class="`${index === selectedIndex? 'active' : ''}`">{{tab}}</li>
                    </ul>
                </div>
                <div class="content">
                    <SafetyPolicy v-if="displayIndex === 0" />
                    <HealthPolicy v-if="displayIndex === 1" />
                    <EnvironmentalProtection v-if="displayIndex === 2" />
                    <WasteMgt v-if="displayIndex === 3" />
                    <QtyAss v-if="displayIndex === 4" />
                    <QtyAssPol v-if="displayIndex === 5" />
                    <Csr v-if="displayIndex === 6" />
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
    data() {
        return {
            tabs: [
                'Safety Policy statement',
                'Health Policy',
                'Environmental protection policy',
                'Waste management policy',
                'Quality assurance statement',
                'Quality assurance policy',
                'Community social responsibilty'
            ],
            selectedIndex: 0,
            displayIndex: 0
        }
    },
    created () {
        
    },
    mounted () {
      this.selectTab(0)
    },
    methods: {
      selectTab(i) {
        this.selectedIndex = i;
        this.displayIndex = this.selectedIndex;
      }
    }
}
</script>

<style lang="scss" scoped>
.hero {
    position: relative;
    padding: 6rem 0;

    ._inner {
        display: flex;
        justify-content: space-between;
        width: 94%;
        margin-left: auto;

        & .text {

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
                margin-bottom: 100px;
            }

            & p {
                font-size: 18px;
                line-height: 30px;
            }
        }
    }
}

.tab-content {
    display: flex;
    justify-content: space-between;
    column-gap: 30px;
}

.tab {
    max-width: 28%;
    ul {
        li {
            padding: 10px 20px;
            margin-bottom: 15px;
            cursor: pointer;

            &.active {
                background-color: #f4f5f5;
                font-family: "Gilroy Medium";
            }

            &:hover {
                font-family: "Gilroy Medium";
            }
        }
    }
}

.content {
    width: 80%;
}

@media screen and (max-width: 1280px) {
    .hero ._inner .text {
        h1 {
            line-height: 50px;
            font-size: 3rem;
        }
    }
}

@media screen and (max-width: 600px) {
    .tab-content {
        flex-direction: column;
    }

    .tab {
        max-width: 100%;
        overflow: scroll;
        margin-bottom: 30px;

        ul {
            display: flex;
        }

        &::-webkit-scrollbar {
            width: 0;
            height: 3px;
        }

        &::-webkit-scrollbar-track {
            background: #f1f1f1;
        }


        &::-webkit-scrollbar-thumb {
            background: #888;
        }
    }

    .content {
        width: 100%;
    }
}
</style>