<template>
  <div class="container-fluid">
    <!-- header top -->
    <nav>
        <div class="d-flex justify-content-between border-bottom align-items-center">
            <div class="flex-fill">
                <select class="form-select eb_color eb_width border-light">
                    <option selected>Language</option>
                    <option value="1">English</option>
                    <option value="2">Italian</option>
                    <option value="3">Spanish</option>
                </select>
            </div>
            <div class="d-flex justify-content-evenly flex-fill">
                <ListLinks/>
                <div class="d-flex align-items-center">
                    <ul class="d-flex list-unstyled pt-3 px-1 align-items-center">
                        <li class="px-2" v-for="icon in icons" :key="icon.id">
                            <i class="eb_color" :class="['fa-brands', icon.name]"></i>
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
                <input id="textCourses" type="text" class="border-0 ms-1 eb_wid_inp">
                <span class="bg-primary border-0 rounded-0 input-group-text"><i class="fa-solid fa-search text-white"></i></span>
            </div>

            <ListLogin/>

            <div class="d-flex align-items-center">
                <button class="btn btn-primary rounded-5 mb-3 mx-4">SIGN-UP</button>
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
    @import '../style/vars.scss';
    .eb_color{
        color: $color-gray-text;
    }
    .eb_width{
        width: 150px;
    }
    .eb_wid_inp{
        width: 400px!important;
        background-color: $bg-card-input;
    }

</style>