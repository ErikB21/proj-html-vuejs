<template>
    <div class="d-flex p-0 container all_card flex-wrap">
        <div v-for="card in cards" :key="card.id" class="card">
            <img :src="card.img" class="card-img-top" :alt="card.name">
            <div class="p-2 card-body d-flex flex-column">
                <span class="pb-3">{{card.course}}</span>
                <h6 class="card-title">{{card.name}}</h6>
            </div>
            <div class="pt-2 border-top card-body d-flex justify-content-between mb-2">
                <p>{{card.date}}</p>
                <p class="text-dark fw-bold">{{card.cost}}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ComponentPopularCourses',
    data(){
        return{
            cards: [
                {
                    img: require('@/assets/images/photo-1461749280684-dccba630e2f6-272x161.jpeg'),
                    course: 'Apache >',
                    name: 'Web Coding and Apache Basics',
                    date: '6 hours',
                    cost: 'Free'
                },
                {
                    img: require('@/assets/images/cat_2-544x322.jpg'),
                    course: 'Art >',
                    name: 'Real Things Art Painting by Jason Ni',
                    date: '6 hours',
                    cost: '$45'
                },
                {
                    img: require('@/assets/images/course-preview-544x322.jpg'),
                    course: 'Software Development >',
                    name: 'Basics of Masterstudy',
                    date: '6 hours',
                    cost: 'Free'
                },
                {
                    img: require('@/assets/images/photo-1496307042754-b4aa456c4a2d-544x322.jpeg'),
                    course: 'Electronic',
                    name: 'How to be a DJ? Make Electronic Music',
                    date: '6 hours',
                    cost: '$49'
                },
                {
                    img: require('@/assets/images/photo-1416339134316-0e91dc9ded92-scaled-544x322.jpeg'),
                    course: 'Communication >',
                    name: 'Design Instruments for Communication',
                    date: '6 hours',
                    cost: "''"
                },
                {
                    img: require('@/assets/images/cathryn-lavery-67852-unsplash-544x322.jpg'),
                    course: 'Art >',
                    name: 'Make your Concept Right and Beautiful',
                    date: '6 hours',
                    cost: '$70'
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../style/vars.scss';
    .all_card{
        width: 100%;
        .card{
            width: calc(100% / 6 - 10px)!important;
            margin: 5px;
            span, p{
                color: $color-gray-text;
            }
        }
    }
</style>