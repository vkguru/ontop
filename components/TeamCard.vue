<template>
    <div class="team-card">
        <img :src="require(`~/assets/img/${imageName}`)" :alt="imageName" />
        <div>
            <h5>{{staffName}}</h5>
            <p>{{qualification}}</p>
            <p>{{position}}</p>
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
        position: String
    }
}
</script>

<style lang="scss" scoped>
.team-card {
    max-width: 280px;
    text-align: center;

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

@media screen and (max-width: 600px) {
    .team-card {
        max-width: 100%;

        img {
            width: 100%;
        }
    }
}
</style>