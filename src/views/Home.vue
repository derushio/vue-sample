<template lang='pug'>
#home
    section.section.main
        h2 Home
        hello-world(msg='Have a good time.')
</template>

<script lang='ts'>
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from '@/components/HelloWorld.vue';

@Component({
    components: {
        HelloWorld,
    },
})
export default class Home extends Vue {}
</script>

<style lang='scss' scoped>
@import 'variable';

#home {
    .main {
        max-width: 900px;
        margin-left: auto; margin-right: auto;
    }
}
</style>
