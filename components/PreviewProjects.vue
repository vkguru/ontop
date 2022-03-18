<template>
    <div class="project_">
        <img :src="require(`~/assets/img/${image}`)" :alt="image"/>
        <div class="content">
            <h4>{{title}}</h4>
            <p>{{location}}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "PreviewProjects",
    props: {
        image: String,
        title: String,
        location: String
    }
}
</script>

<style lang="scss" scoped>
.project_ {
    width: 320px;

    // & img {
    //     width: 100%;
    // }

    & .content {
        padding: 20px 0;

        & h4 {
            font-family: 'Aeonik TRIAL';
            font-size: 20px;
            padding-bottom: 12px;
        }
    }
}
</style>