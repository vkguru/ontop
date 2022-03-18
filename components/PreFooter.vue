<template>
    <div class="preft">
        <div class="ot-container flex">
            <div class="text">
                <h3>Let’s handle your next construction project</h3>
                <div class="_cta">
                    <nuxt-link class="ot-cta_deep" to="/contact-us">Contact us</nuxt-link>
                    <svg width="73" height="25" viewBox="0 0 73 25" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path opacity="0.3" fill-rule="evenodd" clip-rule="evenodd" d="M59.8612 24.5347C59.1862 23.8967 59.1651 22.8417 59.8141 22.1782L69.2808 12.5L59.8141 2.82185C59.1651 2.15834 59.1862 1.10327 59.8612 0.465285C60.5361 -0.172704 61.6094 -0.152017 62.2584 0.511493L72.29 10.7672C73.2367 11.735 73.2367 13.265 72.29 14.2328L62.2584 24.4885C61.6094 25.152 60.5361 25.1727 59.8612 24.5347ZM45.0259 24.5347C44.351 23.8967 44.3299 22.8417 44.9789 22.1781L54.4456 12.5L44.9789 2.82185C44.3299 2.15834 44.351 1.10327 45.0259 0.465284C45.7009 -0.172705 46.7742 -0.152018 47.4232 0.511491L57.4548 10.7672C58.4015 11.735 58.4015 13.265 57.4548 14.2328L47.4232 24.4885C46.7742 25.152 45.7009 25.1727 45.0259 24.5347ZM30.1437 22.1781C29.4947 22.8417 29.5158 23.8967 30.1907 24.5347C30.8657 25.1727 31.939 25.152 32.588 24.4885L42.6196 14.2328C43.5662 13.265 43.5662 11.735 42.6196 10.7672L32.588 0.51149C31.939 -0.152019 30.8657 -0.172706 30.1907 0.465283C29.5158 1.10327 29.4947 2.15834 30.1437 2.82185L39.6104 12.5L30.1437 22.1781ZM15.3555 24.5347C14.6806 23.8967 14.6595 22.8417 15.3085 22.1781L24.7752 12.5L15.3085 2.82185C14.6595 2.15834 14.6806 1.10327 15.3555 0.465281C16.0305 -0.172708 17.1038 -0.152021 17.7528 0.511489L27.7844 10.7672C28.731 11.735 28.731 13.265 27.7844 14.2328L17.7528 24.4885C17.1038 25.152 16.0305 25.1727 15.3555 24.5347ZM0.47332 22.1781C-0.17569 22.8417 -0.154648 23.8967 0.520325 24.5347C1.19529 25.1727 2.26859 25.152 2.91759 24.4885L12.9492 14.2328C13.8958 13.265 13.8958 11.735 12.9492 10.7672L2.9176 0.511488C2.26859 -0.152022 1.19529 -0.172709 0.520327 0.46528C-0.154646 1.10327 -0.175688 2.15834 0.473322 2.82185L9.93996 12.5L0.47332 22.1781Z" fill="url(#paint0_linear_195_5323)"/>
                        <defs>
                        <linearGradient id="paint0_linear_195_5323" x1="73" y1="13" x2="-10" y2="13" gradientUnits="userSpaceOnUse">
                        <stop stop-opacity="0"/>
                        <stop offset="1" stop-color="#9B0000"/>
                        </linearGradient>
                        </defs>
                    </svg>
                </div>
            </div>
            <div class="metrics">
                <span>
                    <h4>20+</h4>
                    <p>Client Projects</p>
                </span>

                <span>
                    <h4>13+</h4>
                    <p>Clients</p>
                </span>

                <span>
                    <h4>19.8yrs</h4>
                    <p>Average staff experience</p>
                </span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Preft"
}
</script>

<style lang="scss" scoped>
.preft {
    padding: 100px 0 200px;

    & .flex {
        column-gap: 150px;
    }

    & ._cta {
        margin-top: 40px;

        & a {
            margin-right: 80px;
        }
    }
}

.text {
    max-width: 600px;
    line-height: 55px;

    & h3 {
        font-size: 48px;
        font-weight: 400;
        font-family: "Aeonik TRIAL";
    }
}

.metrics {
    position: relative;
    max-width: 450px;
    width: 100%;

    & span {
        display: flex;
        flex-direction: column;
        padding: 42px 18px;
        background-color: #FFFFFF;
        box-shadow: -1px 2px 24px 14px rgba(0, 0, 0, 0.04);
        border-radius: 8px;
        margin: 5px;
        text-align: center;

        & h4 {
            font-size: 48px;
            padding-bottom: 15px;
        }

        & p {
            font-family: "Gilroy Medium";
        }

        &:nth-child(1) {
            width: 180px;
            margin-bottom: 16px;
        }

        &:nth-child(2) {
            width: 180px;
        }

        &:nth-child(3) {
            position: absolute;
            top: 45px;
            right: 20px;
            width: 220px;
            padding: 80px 0;
        }
    }
}

@media screen and (max-width: 768px) {
    .metrics {
        & span {
            &:nth-child(2) {
                margin-top: 250px;
            }

            &:nth-child(3) {
                margin-top: 120px;
            }
        }
    }
}

@media screen and (max-width: 600px) {
    .flex {
        flex-direction: column;
    }
}
</style>