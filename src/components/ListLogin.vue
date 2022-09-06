<template>
    <div class="d-flex align-items-center">
        <ul class="d-flex justify-content-between list-unstyled">
            <li class="px-2" v-for="login in logins" :key="login.id">
                <a class="text-decoration-none text-dark" href="#">
                    <i class="text-primary" :class="login.icon"></i>
                    <span class="ps-1">{{login.link}}</span>
                </a>
            </li>
        </ul>
    </div>
    
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