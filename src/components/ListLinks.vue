<template>
    <li class="px-3">
        <a class="text-decoration-none text-dark" href="#">{{item}}</a>
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

<style>

</style>