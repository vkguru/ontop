<template>
    <div class="projects">
        <header>
            <h2>{{title}}</h2>
            <h4>{{location}}</h4>
            <p>{{description}}</p>
        </header>
        <div class="works">
            <img 
                v-for="(image, index) in images" :key="index"
                :src="require(`~/assets/img/${image}`)" :alt="image"
            />
        </div>
    </div>
</template>

<script>
import Header from './Header.vue'
export default {
  components: { Header },
    name: "PortfolioCard",
    props: {
        title: String,
        description: String,
        location: String,
        images: Array
    }
}
</script>

<style lang="scss" scoped>
.projects {
    margin-bottom: 30px;
}

header {
    margin-bottom: 30px;

    & h2 {
        font-family: 'Aeonik TRIAL';
        font-size: 36px;
        font-weight: 400;
        padding-bottom: 12px;
    }

    & h4 {
        font-family: 'Aeonik TRIAL';
        font-size: 20px;
        font-weight: 400;
        padding-bottom: 12px;
    }

    & p {
        max-width: 800px;
    }
}

.works {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    column-gap: 30px;

    & img {
        width: 345px;
        margin-bottom: 30px;
    }
}

@media screen and (min-width: 1448px) {
    .works {
        // max-width: 1200px;
    }
}
</style>