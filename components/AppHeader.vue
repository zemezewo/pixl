<template>
    <div>
        <header>
            <!-- LOGO -->
            <a href="index.html">pixl.</a>
            <!-- LOGO -->
            <Search v-if="isUsersPath"/>
        </header>
    </div>
</template>
<script>
    export default {
        name: 'AppHeader',
        data() {
            return {
                type: false
            }
        },
        computed:{
            isUsersPath(){
                return  this.$route.path==='/List'
            }
        }
    }
</script>