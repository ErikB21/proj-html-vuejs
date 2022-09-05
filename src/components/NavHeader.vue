<template>
  <div class="container-fluid">
    <!-- header top -->
    <nav>
        <div class="d-flex justify-content-between border-bottom align-items-center">
            <div class="flex-fill">
                <select class="form-select eb_width border-light">
                    <option selected>Language</option>
                    <option value="1">English</option>
                    <option value="2">Italian</option>
                    <option value="3">Spanish</option>
                </select>
            </div>
            <div class="d-flex justify-content-evenly flex-fill">
                <div class="d-flex align-items-center">
                    <ul class="d-flex list-unstyled pt-3 align-items-center">
                        <ListLinks v-for="link in links" :key="link.id"  :item="link.title" />
                    </ul>
                </div>
                <div class="d-flex align-items-center">
                    <ul class="d-flex list-unstyled pt-3 px-1 align-items-center">
                        <li class="px-2" v-for="icon in icons" :key="icon.id">
                            <i :class="['fa-brands', icon.name]"></i>
                        </li>
                    </ul>
                </div>
            </div>
        </div>

        <!-- header bottom -->
        <div class="d-flex pt-3 align-items-center justify-content-between">
            <div class="px-2">
                <img src="../assets/images/MasterStudy_logo.svg" alt="">
            </div>
            <div class="d-flex pb-2 px-2 align-items-center">
                <label class="d-flex align-items-center" for="textCourses">
                    <i class="px-1 fa-solid fa-bars"></i>
                    <span>CATEGORY</span>
                </label>
                <input id="textCourses" type="text" class="ms-1 eb_wid_inp">
                <span class="bg-primary input-group-text"><i class="fa-solid fa-search text-white"></i></span>
            </div>
            <div class="list d-flex align-items-center">
                <ul class="list-unstyled">
                    <ListLogin/>
                </ul>
            </div>
            <div class="d-flex align-items-center">
                <button class="btn btn-primary mb-3 mx-4">SIGN-UP</button>
                <i class="fa-regular fa-bookmark mb-3"></i>
            </div>    
        </div>
    </nav>
  </div>
</template>

<script>
import ListLinks from './ListLinks.vue';
import ListLogin from './ListLogin.vue';
export default {
    name: "NavHeader",
    components: { ListLinks, ListLogin },
    data(){
        return{
            links:[
                {
                    title: 'Courses',
                    url: '#',
                    active: false
                },
                {
                    title: 'Zoom',
                    url: '#',
                    active: false
                },
                {
                    title: 'Pages',
                    url: '#',
                    active: false
                },
                {
                    title: 'Bundles',
                    url: '#',
                    active: false
                },
                {
                    title: 'Course Formats',
                    url: '#',
                    active: false
                },
                {
                    title: 'Add Course',
                    url: '#',
                    active: false
                },
                {
                    title: 'Demo',
                    url: '#',
                    active: false
                }
            ],
            icons:[
               {
                name: 'fa-twitter'
               },
               {
                name: 'fa-instagram'
               },
               {
                name: 'fa-behance'
               },
               {
                name: 'fa-dribbble'
               },
               {
                name: 'fa-simplybuilt'
               },
               {
                name: 'fa-git'
               },
               {
                name: 'fa-linkedin'
               },
               {
                name: 'fa-pinterest'
               },
            ],
        }
    }
    
    
}
</script>

<style scoped lang="scss">
    .eb_width{
        width: 150px;
    }
    .eb_wid_inp{
        width: 500px!important;
    }

</style>