<template>
    <div class="text_eb_color m-auto pt-4">
        <div class="row justify-content-between px-3 py-2">

            <div class="col-3">
                <h4 class="text-dark pb-2">About</h4>
                <p><a class="text-decoration-none" href="">Masterstudy</a> is Education WordPress theme featured by Learning Management System (LMS) for online education.<br/>Developed by <a class="text-decoration-none" href="">Sylemix Themes</a>.</p>
                <div>
                    <i class="pe-2" v-for="icon in icons" :key="icon.id" :class="['fa-brands', icon.icon ]"></i>
                </div>
            </div>

            <div class="col-3">
                <h4 class="text-dark pb-2">Contact</h4>
                <p>Usa, California 20, First Avenue, California</p>
                <div class="d-flex flex-column">
                    <span>Tel.: +1 212 458 300 32</span>
                    <span>Fax.: +1 212 375 24 14</span>
                </div>
                <div class="pt-2">
                    <span>info@masterstudy.com</span>
                </div>
            </div>

            <div class="col-3">
                <h4 class="text-dark pb-2">Pages</h4>
                <ListPagesFooter/>
            </div>

            <div class="col-3">
                <h4 class="text-dark pb-2">Blog</h4>
                <ListBlogFooter/>
            </div>
        </div>
    </div>
</template>
    
<script>
import ListPagesFooter from './components/ListPagesFooter.vue';
import ListBlogFooter from './components/ListBlogFooter.vue';
export default {
    name: "FooterComponent",
    data() {
        return {
            icons: [
                {
                    icon: "fa-facebook"
                },
                {
                    icon: "fa-twitter"
                },
                {
                    icon: "fa-instagram"
                }
            ]
        };
    },
    components: { ListPagesFooter, ListBlogFooter }
}
</script>

<style scoped lang="scss">
    @import './style/vars.scss';
    .text_eb_color{
        width: 80vw;
        color: $color-gray-text;
    }
</style>