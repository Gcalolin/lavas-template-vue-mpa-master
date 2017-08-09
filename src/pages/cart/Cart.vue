<template>
    <div>我的购物车</div>
</template>

<script>
    import { mapActions } from 'vuex';
    
    export default {
        name: 'cart',
        props: {},
        methods: {
            ...mapActions('appShell/appBottomNavigator', [
                'showBottomNav',
                'activeBottomNav'
            ])
        },
        activated() {
            this.activeBottomNav('cart');
            this.showBottomNav();
        }
    }
</script>

<style lang="scss" scoped>
    
</style>