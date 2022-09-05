<template>
    <main class="container-fluid px-0">
        <!-- section start investing in you -->
        <div class="d-flex eb_width_section m-auto align-items-center pt-5">
            <div>
                <h2>Start Investing in You</h2>
                <p>With over 1200 courses in 18 subjects, you're guaranteed to find something that's right for you.</p>
                <button class="btn btn-primary">JOIN FOR FREE</button>
            </div>
            <div>
                <img src="../assets/images/base.png" alt="">
            </div>
        </div>
        <CardCertificate/>
        <ComponentPhotoCourses/>
        <div class="d-flex bg_personal align-items-center pt-5">
            <div class="eb_width_section mx-auto">
                <h2>Limitless learning, more possibilities</h2>
                <p>Online courses open the opportunity for learning to almost anyone, regardless of their sheduling commitments.</p>
                <button class="btn btn-primary">READ MORE</button>
            </div>
        </div>
        <div class="container-fluid">
            <h2 class="text-center pt-3 pb-5">Recent Courses</h2>
            <ListRecentCourse class="pb-5"/>
            <CardRecentCourses/>
        </div>
    </main>
</template>

<script>
import CardCertificate from './CardCertificate.vue';
import ComponentPhotoCourses from './ComponentPhotoCourses.vue';
import ListRecentCourse from './ListRecentCourse.vue';
import CardRecentCourses from './CardRecentCourses.vue';
export default {
    name: "MainContent",
    components: { CardCertificate, ComponentPhotoCourses, ListRecentCourse, CardRecentCourses }
}
</script>

<style scoped lang="scss">
    .eb_width_section{
        width: 65vw;
    }
    .bg_personal{
        height: 400px;
        background-image: url('../assets/images/Untitled-1-1-1-1-1.png');
        background-position-y: bottom;
        background-size: cover;
        margin: 0 0 30px;
        h2, p{
            width: 340px;
        }
    }
</style>