<template lang='pug'>
.hello-world
    .title
        h3 Hello world.
        p {{ msg }}

    .box
        p {{ human.name }}
        p {{ human.age }}歳
</template>

<script lang='ts'>
import { Component, Vue, Prop } from 'vue-property-decorator';

import Human from '@/models/Human';

@Component
export default class HelloWorld extends Vue {
    @Prop({ type: String, default: () => '' })
    protected msg?: string;
    @Prop({ type: Object, required: true})
    protected human?: Human;
}
</script>

<style lang='scss' scoped>
@import 'variable';

.hello-world {
    .title {
        margin-bottom: 1rem;
    }
}
</style>
