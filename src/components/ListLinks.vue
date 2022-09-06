<template>
    <div class="d-flex align-items-center">
        <ul class="cl-effect-13 d-flex list-unstyled pt-3 align-items-center">
            <li v-for="link in links" :key="link.id" class="cl-effect-13 px-3">
                <a class="text-decoration-none eb_color" href="#">{{link.title}}</a>
            </li> 
        </ul>
    </div>       
</template>

<script>
export default {
    name: 'ListComponent',
    data(){
        return{
            links:[
                {
                    title: 'Courses',
                    url: '#',
                },
                {
                    title: 'Zoom',
                    url: '#'
                },
                {
                    title: 'Pages',
                    url: '#'
                },
                {
                    title: 'Bundles',
                    url: '#'
                },
                {
                    title: 'Course Formats',
                    url: '#'
                },
                {
                    title: 'Add Course',
                    url: '#'
                },
                {
                    title: 'Demo',
                    url: '#'
                }
            ],
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../style/vars.scss';
    
    .cl-effect-13{
        position: relative;
        .cl-effect-13 a {
            -webkit-transition: color 0.3s;
            -moz-transition: color 0.3s;
            transition: color 0.3s;
            &::before {
                position: absolute;
                top: 50%;
                left: 50%;
                color: transparent;
                content: '•••';
                text-shadow: 0 0 transparent;
                font-size: 1.2em;
                -webkit-transition: text-shadow 0.3s, color 0.3s;
                -moz-transition: text-shadow 0.3s, color 0.3s;
                transition: text-shadow 0.3s, color 0.3s;
                -webkit-transform: translateX(-50%);
                -moz-transform: translateX(-50%);
                transform: translateX(-50%);
                pointer-events: none;
            }
            &:hover::before,
            &:focus::before {
                color: $color-fantastic;
                text-shadow: 10px 0 #fff, -10px 0 #fff;
            }

            &:hover,
            &:focus {
                color: black;
            }
        }
    }
    
    .eb_color{
        color: $color-gray-text;
    }
</style>