<template>
    <ul class="list-unstyled d-flex justify-content-center align-items-center">
        <li class="px-2" v-for="link in links" :key="link.id">
            <a class="text-decoration-none" href="">{{link.name}}</a>
        </li>
    </ul>
</template>

<script>
export default {
    name: 'ListRecentCourses',
    data(){
        return{
            links:[
                {
                    name: 'All Categories',
                    active: true
                },
                {
                    name: 'Art',
                    active: false
                },
                {
                    name: 'Exercise',
                    active: false
                },
                {
                    name: 'Material Design',
                    active: false
                },
                {
                    name: 'Music',
                    active: false
                },
                {
                    name: 'Photography',
                    active: false
                },
                {
                    name: 'Software Development',
                    active: false
                }
            ]
        }
    }
}
</script>

<style>

</style>