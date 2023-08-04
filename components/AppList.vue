<template>
    <ul>
        <!-- <AppCard v-for="item in vids.items" :key="item.id" /> -->
        <li>Hello</li>
    </ul>
</template>
<script>
import AppCard from './AppCard.vue';

    export default {
    name: 'AppList',
    props: [
        vids
    ],
    data() {
        return {
            
        };
    },
    components: { AppCard }
}
</script>