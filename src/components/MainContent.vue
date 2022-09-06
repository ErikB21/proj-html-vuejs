<template>
    <main class="container-fluid px-0">

        <!-- section start investing in you -->
        <ComponentInitMain/>

        <!-- componente card delle certificazioni -->
        <CardCertificate/>

        <!-- componente card del mosaico di foto -->
        <ComponentPhotoCourses/>

        <!-- sezione jumbotron -->
        <div class="d-flex bg_personal align-items-center pt-5">
            <div class="eb_width_section mx-auto">
                <h2>Limitless learning, more possibilities</h2>
                <p>Online courses open the opportunity for learning to almost anyone, regardless of their sheduling commitments.</p>
                <button class="btn btn-primary rounded-5 ">READ MORE</button>
            </div>
        </div>

        <!-- sezione corsi recenti -->
        <div class="container-fluid">
            <h2 class="text-center pt-3 pb-5">Recent Courses</h2>

            <!-- componente sezione corsi recenti (lista link) -->
            <ListRecentCourse class="pb-5"/>

            <!-- componente sezione corsi recenti (card)  -->
            <CardRecentCourses/>
            <div class="text-center">
                <button class="btn btn-primary rounded-5 my-5">SHOW ALL</button>
            </div>
        </div>

        <!-- componente we are proud -->
        <ComponentWeProud/>

        <!-- sezione subscribe -->
        <div class="container-fluid eb_bg_color text-white py-5">
            <div class="eb_width_subscribe row m-auto justify-content-center align-items-center">
                <div class="col-6">
                    <h4>Subscribe our newsletter</h4>
                    <p>There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, or randomised words</p>
                </div>
                <div class="col-6">
                    <label for="basic-url" class="form-label">YOUR E-MAIL ADDRESS</label>
                    <div class="input-group mb-3">
                        <input type="email" class="form-control" id="basic-url" aria-describedby="basic-addon3">
                        <span class="bg-primary text-white rounded-0 border-0 input-group-text" id="basic-addon3">SUBSCRIBE</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- componente popular course -->
        <div class="m-auto py-5 eb_bg_section_3">
            <h2 class="h1 py-2 text-center">Popular courses</h2>
            <p class="py-2 text-center">Discover our most popular courses for self learning</p>
            <ComponentPopularCourses/>
            <div class="d-flex justify-content-center align-items-center pt-5 pb-3">
                <button class="btn btn-light mx-1 rounded-0"><i class="fa-solid fa-chevron-left"></i></button>
                <button class="btn btn-light rounded-0"><i class="fa-solid fa-chevron-right"></i></button>
            </div>
        </div>

        <!-- componente square business -->
        <SquareBusiness/>

        <!-- componente end main -->
        <ComponentEndMain/>
    </main>
</template>

<script>
import CardCertificate from './CardCertificate.vue';
import ComponentPhotoCourses from './ComponentPhotoCourses.vue';
import ListRecentCourse from './ListRecentCourse.vue';
import CardRecentCourses from './CardRecentCourses.vue';
import ComponentWeProud from './ComponentWeProud.vue';
import ComponentPopularCourses from './ComponentPopularCourses.vue';
import SquareBusiness from './SquareBusiness.vue';
import ComponentEndMain from './ComponentEndMain.vue';
import ComponentInitMain from './ComponentInitMain.vue';
export default {
    name: "MainContent",
    components: {
    CardCertificate,
    ComponentPhotoCourses,
    ListRecentCourse,
    CardRecentCourses,
    ComponentWeProud,
    ComponentPopularCourses,
    SquareBusiness,
    ComponentEndMain,
    ComponentInitMain
}
}
</script>

<style scoped lang="scss">
    @import '../style/vars.scss';
    
    .bg_personal{
        height: 400px;
        background-image: url('../assets/images/Untitled-1-1-1-1-1.png');
        background-position-y: center;
        background-repeat: no-repeat;
        background-size: 100%;
        margin: 0 0 30px;
        .eb_width_section{
            width: 65vw;
            h2, p{
                width: 340px;
            }
            p{
                color:$color-gray-text;
            }
        }
        
    }  
    .eb_bg_color{
        background-color: $bg-section-2;
        .eb_width_subscribe{
            width: 65vw;
        }
    }
    .eb_bg_section_3{
        background-color: $bg-section;
        p{
            color:$color-gray-text;
        }
        i{
            color: $color-gray-text;
        }
    }
</style>