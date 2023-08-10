<template>
    <ul>
        <AppCard v-for="item in vids.items" :key="item.id" />
    </ul>
</template>
<script>
import AppCard from './AppCard.vue';

    export default {
    name: 'AppList',
    props: {
        vids: Object,        
    },
    data() {
        return {
            
        };
    },
    components: { AppCard }
}
</script>