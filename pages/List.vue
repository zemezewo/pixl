<style lang="scss">

    @import "../assets/scss/main.scss";
    @import "../assets/scss/pages/video-list";

</style>
<template>
    <div>
        <AppHeader />

        <!-- LIST -->
        <ul id="videoList">

        </ul>
        <!-- LIST -->
    </div>
</template>

<script>
import AppHeader from '~/components/AppHeader.vue';

    export default {
    components: { AppHeader }
}
</script>