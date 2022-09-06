<template>
    <ul class="list-unstyled">
        <li v-for="blog in blogs" :key="blog.id" class="d-flex my-2 align-items-center">
            <div class="pe-3">
                <img :src="blog.img" :alt="blog.title">
            </div>
            <div>
                <ul class="list-unstyled eb_fs">
                    <li><a class="text_eb_color text-decoration-none" href="">{{blog.title}}</a></li>
                    <li class="text_eb_color2">{{blog.text}}</li>
                </ul>
            </div>
        </li>
    </ul>
</template>

<script>
export default {
    name: 'ListBlogfooter',
    data(){
        return{
            blogs:[
                {
                    img: require('@/assets/images/photo-1517520287167-4bbf64a00d66-69x69.jpeg'),
                    title: 'Our Main target is to "Developing Yourself as a Leader"',
                    text: '- August 9, 2018'
                },
                {
                    img: require('@/assets/images/photo-1490376840453-5f616fbebe5b-69x69.jpeg'),
                    title: 'Those Other College Expense You Aren\'t Thinking About',
                    text: '- June 3, 2015'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../style/vars.scss';
    .text_eb_color{
        color: $color-gray-text;
    }
    .text_eb_color2{
        color: $color-gray-text-light;
    }
    .eb_fs{
        font-size: 0.9rem;
    }
</style>