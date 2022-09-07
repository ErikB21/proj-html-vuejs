<template>
    <div class="d-flex p-0 container all_card flex-wrap">
        <div v-for="card in cards" :key="card.id" class="card  position-relative">
            <img :src="card.img" class="card-img-top" :alt="card.name">
            <span class="new text-light p-1 rounded-2">{{card.new}}</span>
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
                    cost: '$45',
                    new: 'NEW'
                },
                {
                    img: require('@/assets/images/course-preview-544x322.jpg'),
                    course: 'Software Development >',
                    name: 'Basics of Masterstudy',
                    date: '6 hours',
                    cost: 'Free',
                    new: 'HOT'
                },
                {
                    img: require('@/assets/images/photo-1496307042754-b4aa456c4a2d-544x322.jpeg'),
                    course: 'Electronic',
                    name: 'How to be a DJ? Make Electronic Music',
                    date: '6 hours',
                    cost: '$49',
                    new: 'SPECIAL'
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
                    cost: 'Free',
                    new: 'SPECIAL'
                },
                {
                    img: require('@/assets/images/jakob-owens-198234-unsplash-min-1-544x322.png'),
                    course: 'Art >',
                    name: 'How to Work with Legendary RED camera?',
                    date: '6 hours',
                    cost: 'Free',
                    new: 'SPECIAL'
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
    @import '../style/vars.scss';
    .all_card{
        width: 100%;
        .card{
            width: calc(100% / 6 - 10px)!important;
            margin: 5px;
            &:nth-child(2) .new{
                background-color: $color-square-new;
            }
            &:nth-child(3) .new{
                background-color: $color-square-hot;
            }
            &:nth-child(4) .new,
            &:nth-child(10) .new,
            &:nth-child(11) .new{
                background-color: $color-square-special;
            }
            
            .new{
                position: absolute;
                top: 8px;
                right: 8px;
                font-size: 0.8rem;
            }
            span, p{
                color: $color-gray-text;
            }
        }
    }
</style>