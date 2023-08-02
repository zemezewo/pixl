<template>
    <div>
        <header>
            <!-- LOGO -->
            <a href="index.html">pixl.</a>
            <!-- LOGO -->
            <Search v-if="type"/>
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
        }
    }
</script>