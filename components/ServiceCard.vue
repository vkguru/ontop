<template>
    <div class="service-card">
        <img :src="img" :alt="alt" />
        <div class="overlay">
            <h4>{{title}}</h4>
            <p>{{info}}</p>
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

</style>