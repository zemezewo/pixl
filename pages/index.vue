<style lang="scss">
    @import "../assets/scss/main.scss";
    @import "../assets/scss/pages/index";
</style>
<template>
  <div class="main-container">
        <AppHeader />

        <!-- HERO -->
        <div class="flex-container">
            <h3>
                Welcome to <span id="pixl">pixl.</span>
                <span>Explore millions of videos from various channels.</span>
            </h3>
            <a href="channelList.html">Explore.</a>
        </div>
        <!-- HERO -->
  </div>
</template>

<script>
export default {

//   name: 'IndexPage',
//   data () {
//     return {
//       info: null
//     }
//   },
//   mounted ({ app }) {
//     app.$axios.$get('https://www.googleapis.com/youtube/v3/videos?' + new URLSearchParams({
//     key: 'AIzaSyDXxiER1QTuy3RKJxRTPJ6ue',
//     part: 'snippet',
//     chart: 'mostPopular',
//     maxResult: 4,
//     regionCode: "NG"
// }))
//       .then(response => (this.info = response))
//   }

    name: 'IndexPage',
    data () {
        return {
            ffs: 'ffs',
            info: null
        }
        },

//  asyncData ({ app }) {
//    let { data } = axios.$get('/' + new URLSearchParams({
//     key: 'AIzaSyDXxiER1QTuy3RKJxRTPJ6ue',
//     part: 'snippet',
//     chart: 'mostPopular',
//     maxResult: 4,
//     regionCode: "NG"
//     }))
//     .then(response => (this.info = response))
//     .catch(err => console.log(err));
//   }
}

</script>

<style lang="scss">
</style>