<template>
    <div>我的云购</div>
</template>

<script>
    import { mapActions } from 'vuex';
    
    export default {
        name: 'member',
        props: {},
        methods: {
            ...mapActions('appShell/appBottomNavigator', [
                'showBottomNav',
                'activeBottomNav'
            ])
        },
        activated() {
            this.activeBottomNav('member');
            this.showBottomNav();
        }
    }
</script>

<style lang="scss" scoped>
    
</style>