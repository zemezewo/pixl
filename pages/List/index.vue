<style lang="scss">

    @import "../../assets/scss/main.scss";
    @import "../../assets/scss/pages/video-list";

</style>

<template>
    <div>
        <AppHeader />
        <AppList :vids="vids" />
    </div>
</template>

<script>
import AppHeader from '~/components/AppHeader.vue';
import AppList from '~/components/AppList.vue';
import axios from 'axios';


export default {
    components: { AppHeader, AppList },
    asyncData () {
        return axios.get(`https://youtube.googleapis.com/youtube/v3/videos?part=snippet%2Cstatistics&chart=mostPopular&maxResults=32&regionCode=NG&key=AIzaSyDXxiER1QTuy3RKJxRTPJ6ue-kqVLGadSM`)
        .then((res) => {
            return {
                vids: res.data
            }
        })
        .catch((e) => {
            console.log(e)
        })
    }
}
</script>