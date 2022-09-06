<template>
    <ul class="d-flex  flex-wrap align-items-center">
        <li class="eb_width py-2" v-for="link in links" :key="link.id">
            <a class="text-decoration-none text-dark" href="">{{link.title}}</a>
        </li>
    </ul>
</template>

<script>
export default {
    name:'ListPagesFooter',
    data(){
        return{
            links:[
                {
                    title: 'Blog'
                },
                {
                    title: 'Courses'
                },
                {
                    title: 'Home'
                },
                {
                    title: 'Membership A...'
                },
                {
                    title: 'Shortcodes'
                },
                {
                    title: 'Typography'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    li{
        width: 100px;
        font-size: 0.8rem;
    }
</style>