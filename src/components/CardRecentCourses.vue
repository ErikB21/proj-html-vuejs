<template>
    <div class="d-flex container all_card flex-wrap">
        <div v-for="card in cards" :key="card.id" class="card">
            <img :src="card.img" class="card-img-top" :alt="card.name">
            <div class="card-body d-flex flex-column">
                <p>{{card.course}}</p>
                <h5 class="card-title">{{card.name}}</h5>
            </div>
            <div class="border-top card-body d-flex justify-content-between">
                <p>{{card.date}}</p>
                <p>{{card.cost}}</p>
            </div>
        </div>
    </div>
</template>


<script>
export default {
    name:'CardRecentCourses',
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
                {
                    img: require('@/assets/images/photo-1475452779376-caebfb988090-272x161.jpeg'),
                    course: 'Bicycling >',
                    name: 'Road Bike Manual or How to Be a Champion',
                    date: '6 hours',
                    cost: '$20'
                },
                {
                    img: require('@/assets/images/cristian-grecu-762012-unsplash-min-scaled-544x322.jpg'),
                    course: 'Documentary >',
                    name: 'How to Make Beautiful landscape Photos?',
                    date: '6 hours',
                    cost: '$60'
                },
                {
                    img: require('@/assets/images/landscape-544x322.jpg'),
                    course: 'Art >',
                    name: "let's paint Van Gogh's Starry Night",
                    date: '6 hours',
                    cost: '$79'
                },
                {
                    img: require('@/assets/images/12345-1-544x322.png'),
                    course: 'Nvidia >',
                    name: 'Nvidia and UE4 Technologies Practice',
                    date: '6 hours',
                    cost: 'Free'
                },
                {
                    img: require('@/assets/images/jakob-owens-198234-unsplash-min-1-544x322.png'),
                    course: 'Art >',
                    name: 'How to Work with Legendary RED camera?',
                    date: '6 hours',
                    cost: 'Free'
                },
                {
                    img: require('@/assets/images/promo_tf-544x322.jpg'),
                    course: 'Software Development >',
                    name: 'Masterstudy Mobile LMS App',
                    date: '2 hours',
                    cost: 'Free'
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    .all_card{
        width: 100%;
        .card{
            width: calc(100% / 6 - 15px)!important;
            margin: 7.5px;
        }
    }
</style>