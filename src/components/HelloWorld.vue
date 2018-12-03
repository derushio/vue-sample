<template lang='pug'>
.hello-world
    h3 Hello world.
    p {{ msg }}
</template>

<script lang='ts'>
import { Component, Vue, Prop } from 'vue-property-decorator';

@Component
export default class HelloWorld extends Vue {
    @Prop({ type: String, default: () => '' })
    protected msg?: string;
}
</script>

<style lang='scss' scoped>
@import 'variable';

.hello-world {}
</style>
