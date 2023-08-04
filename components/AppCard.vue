<template>
    <li>
        <a href="videoPlayer.html">
            <!-- VIDEO THUMBNAIL -->
            <img src={{ item.snippet.thumbnails.maxres.url }} alt="Video Thumbnail"/>
            <div class="vid-caption">
                <div class="channel-img">
                    <!-- channelPage with channelID, channelID fetches data needed for page-->
                    <a href="channelPage.html"> 
                        <!-- CHANNEL PROFILE PHOTO -->
                        <img src={{ channels.items.snippet.thumbnails.default.url }} alt="Channel Thumbnail"/>
                    </a>
                </div>
                <div class="vid-info">
                    <h3>{{ item.snippet.title }}</h3>
                    <p>{{ channels.items.snippet.Channeltitle }}</p>
                    <p>536K views . ${videoPublished(data)}</p>
                </div>
            </div>
        </a>
    </li>
</template>
<script>
    export default {
        name: 'AppCard',
        props: [ 
            
        ],
        asyncData () {
        return axios.get(`https://youtube.googleapis.com/youtube/v3/channels?part=snippet%2Cstatistics&id=&key=AIzaSyDXxiER1QTuy3RKJxRTPJ6ue-kqVLGadSM` + new URLSearchParams({
            id: item.snippet.channelId
        }))
        .then((res) => {
            return {
                channels: res.data
            }
        })
        .catch((e) => {
            console.log(e)
        })
        },
        data() {
            return {
                
            }
        },
    }
</script>