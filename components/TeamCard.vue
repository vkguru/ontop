<template>
    <div>
        <div class="team-card" @click="openModal">
            <img :src="require(`~/assets/img/${imageName}`)" :alt="imageName" />
            <div>
                <h5>{{staffName}}</h5>
                <p>{{qualification}}</p>
                <p>{{position}}</p>
            </div>
        </div>

        <div class="modal" v-if="open">
            <div class="content">
                <button @click="closeModal">Close</button>
                <div class="_inner">
                    <h4>{{staffName}}</h4>
                    <h5>{{position}}</h5>
                    <p>{{staffBio}}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "TeamCard",
    props: {
        imageName: String,
        staffName: String,
        qualification: String,
        position: String,
        staffBio: String
    },
    data() {
        return {
            open: false
        }
    },
    methods: {
        openModal() {
            this.open = true;
        },
        closeModal() {
            this.open = false;
            console.log(this.close)
        }
    }
}
</script>

<style lang="scss" scoped>
.team-card {
    max-width: 280px;
    text-align: center;
    cursor: pointer;

    & img {
        background-color: #ccc;
    }

    & div {
        padding: 20px;
    }

    & h5 {
        font-family: "Aeonik TRIAL";
        line-height: 30px;
    }

    & p {
        font-size: 14px;

        &:last-child {
            font-family: "Gilroy Medium";
            line-height: 30px;
        }
    }
}

.modal {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    height: 100%;
    width: 100%;
    background: rgba(0,0,0,0.4);
    padding: 30px;
    z-index: 10;

    & .content {
        background: $ot-white;
        width: calc(50% + 120px);
        margin: 100px auto;
        padding: 50px;

        & button {
            background: transparent;
            border: 0;
            font-size: 16px;
            font-family: "Gilroy Medium";
            cursor: pointer;
            padding: 15px 0;
            margin-bottom: 15px;
        }

        & ._inner {
            & h4 {
                font-size: 22px;
            }

            & h5 {
                font-size: 16px;
                margin-bottom: 20px;
            }

            & p {
                font-family: "Gilroy Regular";
                font-size: 1rem;
            }
        }

    }
}

@media screen and (max-width: 600px) {
    .team-card {
        max-width: 100%;

        img {
            width: 100%;
        }
    }
}
</style>