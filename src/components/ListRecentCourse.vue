<template>
    <ul class="cl-effect-1 list-unstyled d-flex justify-content-center align-items-center">
        <li class="rounded-5 p-2" :class="link.active ? 'active':'' " v-for="link in links" :key="link.id">
            <a class="text-decoration-none text-dark" :href="link.url">{{link.name}}</a>
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
                    active: true,
                    url: '#'
                },
                {
                    name: 'Art',
                    active: false,
                    url: '#',
                },
                {
                    name: 'Exercise',
                    active: false,
                    url: '#',
                },
                {
                    name: 'Material Design',
                    active: false,
                    url: '#',
                },
                {
                    name: 'Music',
                    active: false,
                    url: '#',
                },
                {
                    name: 'Photography',
                    active: false,
                    url: '#',
                },
                {
                    name: 'Software Development',
                    active: false,
                    url: '#'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../style/vars.scss';
    
    .cl-effect-1 a::before,
    .cl-effect-1 a::after {
        display: inline-block;
        opacity: 0;
        -webkit-transition: -webkit-transform 0.3s, opacity 0.2s;
        -moz-transition: -moz-transform 0.3s, opacity 0.2s;
        transition: transform 0.3s, opacity 0.2s;
    }

    .cl-effect-1 a::before {
        margin-right: 10px;
        content: '<';
        color: $color-fantastic;
        -webkit-transform: translateX(20px);
        -moz-transform: translateX(20px);
        transform: translateX(20px);
    }

    .cl-effect-1 a::after {
        margin-left: 10px;
        content: '/>';
        color: $color-fantastic;
        -webkit-transform: translateX(-20px);
        -moz-transform: translateX(-20px);
        transform: translateX(-20px);
    }

    .cl-effect-1 a:hover::before,
    .cl-effect-1 a:hover::after,
    .cl-effect-1 a:focus::before,
    .cl-effect-1 a:focus::after {
        opacity: 1;
        -webkit-transform: translateX(0px);
        -moz-transform: translateX(0px);
        transform: translateX(0px);
    }
</style>