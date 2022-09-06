<template>
    <div class="d-flex eb_width_section m-auto align-items-center pt-5 pb-5">
        <div>
            <h2>Start Investing in You</h2>
            <p>With over 1200 courses in 18 subjects, you're guaranteed to find something that's right for you.</p>
            <button class="btn btn-primary rounded-5">JOIN FOR FREE</button>
        </div>
        <div class="position-relative">
            <img src="../assets/images/base.png" alt="">
            <img class="eb_pos_1" src="../assets/images/book1.png" alt="">
            <img class="eb_pos_2" src="../assets/images/book2.png" alt="">
            <img class="eb_pos_3" src="../assets/images/magnifier.png" alt="">
            <img class="eb_pos_4" src="../assets/images/bubblespeech.png" alt="">
            <img class="eb_pos_5" src="../assets/images/moon.png" alt="">
        </div>
    </div>
</template>

<script>
export default {
    name: 'ComponentInitMain'
}
</script>

<style scoped lang="scss">
    .eb_width_section{
        width: 65vw;
        .eb_pos_1{
            position: absolute;
            top: 21%;
            right: 6%;
        }
        .eb_pos_2{
            position: absolute;
            top: 54%;
            right: 25%;
        }
        .eb_pos_3{
            position: absolute;
            top: 68%;
            right: 12%;
        }
        .eb_pos_4{
            position: absolute;
            top: 10%;
            right: 6%;
        }
        .eb_pos_5{
            position: absolute;
            top: 27%;
            right: 71%;
        }
    }
</style>