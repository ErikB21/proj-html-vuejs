<template>
    <div class="eb_width_section m-auto py-5">
        <div class="my_wid row">
            <div class="col-8 d-flex pe-3 flex-column my_sec_img align-self-center">
                <img src="../assets/images/cat_1-1540x750.jpg" alt="">
                <div class="d-flex justify-content-between align-items-center">
                    <span>Software Development</span>
                    <span>5 courses</span>
                </div>
            </div>
            <div class="col-4 d-flex flex-column justify-content-between my_sec_img2">
                <div class="d-flex flex-column">
                    <img src="../assets/images/cat_2-370x155.jpg" alt="">
                    <div class="d-flex justify-content-between align-items-center">
                        <span>Art</span>
                        <span>8 courses</span>
                    </div>
                </div>
                <div class="d-flex flex-column">
                    <img src="../assets/images/cat_3-370x155.jpg" alt="">   
                <div class="d-flex justify-content-between align-items-center">
                    <span>Material Design</span>
                    <span>5 courses</span>
                </div>
            </div>
        </div>
    </div>
    <div class="row d-flex justify-content-between pt-4 pb-5">
        <div v-for="photo in photosList" :key="photo.id" class="col-4 my_sec_img2">
            <img :src="photo.img" :alt="photo.text">
            <div class="d-flex justify-content-between align-items-center">
                <span>{{photo.text}}</span>
                <span>{{photo.course}}</span>
            </div>
        </div>
    </div>
    </div>
</template>

<script>
export default {
    name: 'ComponentPhotoCourses',
    data(){
        return{
            photosList:[
                // {
                //     img: require('@/assets/images/cat_1-770x375.jpg'),
                //     text: 'Software Development'
                // },
                // {
                //     img: require('@/assets/images/cat_2-740x310.jpg'),
                //     text: 'Art'
                // },
                // {
                //     img: require('@/assets/images/cat_3-740x310.jpg'),
                //     text: 'Material Design'
                // },
                {
                    img: require('@/assets/images/cat_4-740x310.jpg'),
                    text: 'Music',
                    course:'5 courses'
                },
                {
                    img: require('@/assets/images/cat_5-740x310.jpg'),
                    text: 'Exercise',
                    course:'7 courses'
                },
                {
                    img: require('@/assets/images/cat_6-740x310.jpg'),
                    text: 'Photography',
                    course:'4 courses'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    .my_sec_img{
        width: 66.6%;
        img{
            width: 100%;
            height: 100%;
        }
    }
    .my_sec_img2{
        width: calc(100% / 3 - 4px);
        margin: 0 2px;
        // div:first-of-type{
        //     margin-bottom: 4px;
        // }
        // &:nth-of-type(3){
        //     margin-right: 2px;    
        // }

        img{
            width: 100%;
        }
    }
</style>