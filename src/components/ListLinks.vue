<template>
    <li class="px-3">
        <a class="text-decoration-none eb_color" href="#">{{item}}</a>
    </li>    
</template>

<script>
export default {
    name: 'ListComponent',
    props:{
        item: String,
    },
}
</script>

<style scoped lang="scss">
    @import '../style/vars.scss';
    .eb_color{
        color: $color-gray-text;
    }
</style>