<template>
    <div class="service-card">
        <img :src="require(`~/assets/img/${img}`)" :alt="alt" />
        <div class="overlay">
            <div class="content">
                <h4>{{title}}</h4>
                <p>{{info}}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "ServiceCard",
    props: {
        title: String,
        info: String,
        img: String,
        alt: String
    }
}
</script>

<style lang="scss" scoped>
.service-card {
    position: relative;
    display: flex;
    max-width: 370px;
    width: 100%;

    img {
        height: 100%;
        width: 100%;
        border-radius: 8px;
    }

    p {
        display: none;
        transition: 2s display ease-in-out;
    }

    &:hover p {
        display: block;
        transition: 2s display ease-in-out;
    }
}

.overlay {
    position: absolute;
    top: 0;
    background: linear-gradient(180deg, rgba(155, 0, 0, 0.212) 4%, rgba(0, 0, 0, 0.74) 78.12%);
    width: 100%;
    height: 100%;
    border-radius: 8px;

    & .content {
        position: absolute;
        bottom: 20px;
        color: $ot-white;
        padding: 20px;

        & h4  {
            font-size: 1.125rem;
        }

        & p {
            font-size: 1rem;
        }
    }
}

@media screen and (max-width: 768px) {
    .service-card {
        max-width: 47%;
    }
}

@media screen and (max-width: 600px) {
    .service-card {
        max-width: 100%;
    }
}
</style>