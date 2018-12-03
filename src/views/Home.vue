<template lang='pug'>
#home
    section.section.main
        h2 Home
        hello-world(msg='Have a good time.' :human='human')
</template>

<script lang='ts'>
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from '@/components/HelloWorld.vue';

import Human from '@/models/Human';

@Component({
    components: {
        HelloWorld,
    },
})
export default class Home extends Vue {
    protected human = {
        name: 'Taro',
        age: 22,
    } as Human;
}
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
