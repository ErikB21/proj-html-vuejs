<template>
    <div class="m-auto px-5">
        <div class="row justify-content-center py-5 align-items-center">
            <div v-for="item in items" :key="item.id" class="d-flex justify-content-center border mx-5 p-3 align-items-center col-5">
                <div class="px-2">
                    <img :src="item.img" :alt="item.title">
                </div>
                <div>
                    <h3 class="py-2">{{item.title}}</h3>
                    <p class="py-2">{{item.text}}</p>
                    <button class="btn btn-primary">{{item.buttonText}}</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SquareBusiness',
    data(){
        return{
            items: [
                {
                    img: require('@/assets/images/image_box_1-221x231.png'),
                    title: 'Become an Instructor',
                    text: 'Teach what you love, Masterstudy gives you the tools to create a course.',
                    buttonText: 'START TEACHING'
                },
                {
                    img: require('@/assets/images/image_box_2-234x231.png'),
                    title: 'Setup For Business',
                    text: 'Get unlimited access to 2.500 of Udemy\'s top courses for you team.',
                    buttonText: 'DOING BUSINESS'
                }
            ]
        }
    }
}
</script>

<style>

</style>