<template>
    <footer>
        <div class="ft-brand">
            <img src="~/assets/img/logo-white.png" alt="ontop builders logo" />
            <p>We deliver projects that defies all limitations</p>
        </div>
        <div class="ft-info">
            <div class="_link">
                <ul>
                    <li><router-link to="/">Our Services</router-link></li>
                    <li><router-link to="/">Portfolio</router-link></li>
                    <li><router-link to="/">About Us</router-link></li>
                    <li><router-link to="/">Contact Us</router-link></li>
                </ul>
            </div>
            <div class=""></div>
        </div>
    </footer>
</template>

<script>
export default {
    name: "Footer"
}
</script>

<style lang="scss" scoped>
footer {
    background-color: $ot-black;
}
</style>