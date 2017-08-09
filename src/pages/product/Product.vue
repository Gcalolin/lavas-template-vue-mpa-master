<template>
    <div>所有商品</div>
</template>

<script>
    import { mapActions } from 'vuex';
    
    export default {
        name: 'product',
        props: {},
        mounted() {
        },
        methods: {
            ...mapActions('appShell/appBottomNavigator', [
                'showBottomNav',
                'activeBottomNav'
            ])
        },
        activated() {
            this.activeBottomNav('product');
            this.showBottomNav();
        }
    }
</script>

<style lang="scss" scoped>
    
</style>