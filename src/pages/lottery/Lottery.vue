<template>
    <div>
      <!--   <h2>LAVAS</h2>
        <h4>[ˈlɑ:vəz]</h4> -->
        最新揭晓
    </div>
</template>

<script>
import {mapActions} from 'vuex';

export default {
    name: 'lottery',
    props: {},
    methods: {
        ...mapActions('appShell/appBottomNavigator', [
            'showBottomNav',
            'activateBottomNav'
        ])
    },
    // async asyncData() {
    //     await new Promise((resolve, reject) => {
    //         setTimeout(resolve, 500);
    //     });
    // },
    activated() {
        this.activateBottomNav('lottery');
        this.showBottomNav();
    }
};
</script>

<style lang="stylus" scoped>
$text-color := rgba($material-theme.text-color, $material-theme.primary-text-percent)

h2
    margin-top 50%
    font-size 46px
    font-weight 500

h2, h4
    color $text-color
</style>
