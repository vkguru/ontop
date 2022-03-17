<template>
    <div class="equip-card">
        <figure>
            <img :src="require(`~/assets/img/${equipImg}`)" :alt="equipImg" />
        </figure>
        <p>{{equipName}}</p>
    </div>
</template>

<script>
export default {
    name: "EquipCard",
    props: {
        equipImg: String,
        equipName: String
    }
}
</script>

<style lang="scss" scoped>
.equip-card {
    max-width: 280px;
    text-align: center;

    & figure {
        min-height: 373px;
    }

    & p {
        font-size: 14px;
        font-family: "Gilroy Medium";
        line-height: 30px;
    }
}
</style>