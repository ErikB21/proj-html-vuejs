<template>
    <div class="container-fluid m-auto p-5 bg_personal_2 text-center">
        <div class="eb_width m-auto">
            <h2 class="h1 pb-4">We are Proud</h2>
            <p class="fs-5">Certificate courses are instructed by highly educated and qualified instructors who hold doctoral and master's level degrees.</p>
        </div>
        <ul class="d-flex list-unstyled pt-4 justify-content-center align-items-center">
            <li v-for="course in courses" :key="course.id" class="border-end d-flex flex-column px-5 pt-4 align-items-center">
                <h2 class="h1">{{course.number}}</h2>
                <span>{{course.text}}</span>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name:'ComponentWeProud',
    data(){
        return{
            courses:[
                {
                    number: 2000,
                    text: 'STUDENTS'
                },
                {
                    number: 950,
                    text: 'COURSES'
                },
                {
                    number: 1600,
                    text: 'HOURS VIDEO'
                },
                {
                    number: 150,
                    text: 'COUNTRIES REACHED'
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../style/vars.scss';
    .bg_personal_2{
        height: 550px;
        background-image: url('../assets/images/we_proud.png');
        background-position-y: bottom;
        background-repeat: no-repeat;
        background-size: contain;
        background-color: $bg_section;
        .eb_width{
            width: 60%;
            p{
                color: $color-gray-text;
            }
        }
        ul li:last-child{
            border: none!important;
        }
        span{
            color: $color-gray-text;
        }
    }
</style>