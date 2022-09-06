<template>
    <div class="container-fluid px-0 bg_section d-flex justify-content-center align-items-center">
        <div class="square_white d-flex flex-column justify-content-center p-5">
            <h2 class="h1 py-2">Come as you are</h2>
            <p class="py-2 text_eb_color">MasterStudy used in an excellent workshop whether you come as a counselor, advisor, administrator, or faculty member. I am going home empowered. I am looking forward to attending the On Course MasterStudy and the MasetrStudy National Conference next year and facilitating the use of this excellent retention/student success course at my college.</p>
            <div class="py-3 d-flex flex-column">
                <span class="fw-bold">Tim Sab</span>
                <span class="fw-bold eb_fs">General Developer, Stlemix Themes</span>
            </div>
        </div>
        <div class="square_arrow me-4">
            <img src="../assets/images/arrow.png" alt="">
        </div>
    </div>
</template>

<script>
export default {
    name: 'ComponentEndMain'
}
</script>

<style scoped lang="scss">
    @import '../style/vars.scss';
    .bg_section{
        background-image: url(../assets/images/brooke-cagle-224821-unsplash-1-1920x700.jpg);
        background-size: cover;
        height: 600px;
        position: relative;
        .square_white{
            height: 380px;
            width: 550px;
            background-color: white;
            .text_eb_color{
                color: $color-gray-text;
            }
            .eb_fs{
                font-size: 0.7rem;
            }
        }
        .square_arrow{
            width: 30px;
            height: 30px;
            position: absolute;
            top: 40%;
            right: 382px;
            img{
                width: 30px;
                height: 30px;
            }
        }
    }
   

</style>