<template>
    <section class="px-1 pb-4 eb_width_section m-auto d-flex justify-content-between">
        <div class="box" v-for="card in cards" :key="card.id">
            <div class="body">
                <div class="imgContainer">
                    <img :src="card.img" :alt="card.subtitle">
                </div>
                <div class="content d-flex flex-column align-items-center justify-content-center">
                    <div>
                        <i :class="['fa-solid', 'fa-3x', card.icon]" class="pt-2" ></i>
                        <h5 class="pt-2 fw-bold">{{card.title}}</h5>
                        <p class="pt-2">{{card.paragraph}}</p>
                    </div>
                </div>
            </div>
        </div>
        
    </section>
        
</template>

<script>
export default {
    name: 'CardCertificate',
    data(){
        return{
            cards:[
                {
                    icon: 'fa-earth-europe',
                    title: 'WorldWide Recognize',
                    paragraph: 'Our Online course certificates can be used around the world and also in most popular univesities and companies.',
                    img: require('@/assets/images/connections.jpg'),
                    subtitle: ''
                },
                {
                    icon: 'fa-display',
                    title: 'Mostly Online Learning',
                    paragraph: 'Masterstudy online certificates can be obtained in a range of specialized areas and typically take about a year to complete.',
                    img: require('@/assets/images/codee.png'),
                    subtitle: ''
                },
                {
                    icon: 'fa-calendar',
                    title: 'Graduate in as little as 1 Year',
                    paragraph: 'Online post-graduate certificates are a popular way to develop your professional qualifications of Masterstudy.',
                    img: require('@/assets/images/chess.jpg'),
                    subtitle: ''
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../style/vars.scss';

    .eb_width_section{
        width: 65vw;
        margin-inline: auto;
        i{
            color: white;
        }
        .box{
            position: relative;
            width: 300px;
            height: 300px;
            margin: 20px;
            transform-style: preserve-3d;
            perspective: 1000px;
            cursor: pointer;
        }

        .box .body{
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            transform-style: preserve-3d;
            transition: 0.9s ease;
        }

        .box .body .imgContainer{
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            transform-style: preserve-3d;
        }

        .box .body .imgContainer img{
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .box .body .content{
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #333;
            backface-visibility: hidden;
            transform-style: preserve-3d;
            transform: rotateY(180deg);
        }

        .box:hover .body{
            transform: rotateY(180deg);
        }

        .box .body .content div{
            transform-style: preserve-3d;
            padding: 20px;
            background-image: radial-gradient(100% 100% at 100% 0, #5adaff 0, #4D759D 100%);
            transform: translateZ(100px);
        }
    }

</style>