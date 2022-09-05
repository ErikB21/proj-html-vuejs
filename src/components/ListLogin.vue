<template>
    <section class="d-flex justify-content-between">
        <li class="px-2" v-for="login in logins" :key="login.id">
            <a class="text-decoration-none text-dark" href="#">
                <i :class="login.icon"></i>
                <span class="ps-2">{{login.link}}</span>
            </a>
        </li>
    </section>
</template>

<script>
export default {
    name: 'ListLogin',
    data(){
        return{
            logins:[
                {
                    icon: 'fa-solid fa-bullhorn',
                    link: 'Become an instructor'
                },
                {
                    icon: 'fa-solid fa-briefcase',
                    link: 'For Enterprise'
                },
                {
                    icon: 'fa-regular fa-user',
                    link: 'Log In'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">

</style>