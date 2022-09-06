<template>
    <section class="px-1 pb-4 eb_width_section m-auto d-flex justify-content-between">
        <div v-for="card in cards" :key="card.id" class="col-4 eb_card px-5 py-2">
            <i :class="['fa-solid', 'fa-3x', card.icon]" class="pt-2" ></i>
            <h5 class="pt-2">{{card.title}}</h5>
            <p class="pt-2">{{card.paragraph}}</p>
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
                    paragraph: 'Our Online course certificates can be used around the world and also in most popular univesities and companies.'
                },
                {
                    icon: 'fa-display',
                    title: 'Mostly Online Learning',
                    paragraph: 'Masterstudy online certificates can be obtained in a range of specialized areas and typically take about a year to complete.'
                },
                {
                    icon: 'fa-calendar',
                    title: 'Graduate in as little as 1 Year',
                    paragraph: 'Online post-graduate certificates are a popular way to develop your professional qualifications of Masterstudy.'
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
        .eb_card{
            background-color: $bg-card-input;
            width: 32%;
        }
    }
</style>