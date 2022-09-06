<template>
    <div class="m-auto px-5">
        <div class="row justify-content-center py-5 align-items-center">
            <div v-for="item in items" :key="item.id" class="d-flex justify-content-center border mx-5 p-3 align-items-center col-5">
                <div class="px-2">
                    <img :src="item.img" :alt="item.title">
                </div>
                <div class="ps-2">
                    <h3 class="py-2">{{item.title}}</h3>
                    <p class="py-2">{{item.text}}</p>
                    <button class="btn button-50">{{item.buttonText}}</button>
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

<style scoped lang="scss">
    @import '../style/vars.scss';
    p{
        color: $color-gray-text;
    }
    .button-50 {
        appearance: button;
        background-color: #4D759D;
        background-image: none;
        border: 1px solid #4D759D;
        border-radius: 4px;
        box-shadow: #fff 4px 4px 0 0,#4D759D 4px 4px 0 1px;
        box-sizing: border-box;
        color: #fff;
        cursor: pointer;
        display: inline-block;
        font-family: ITCAvantGardeStd-Bk,Arial,sans-serif;
        font-size: 14px;
        font-weight: 400;
        line-height: 20px;
        margin: 0 5px 10px 0;
        overflow: visible;
        padding: 12px 40px;
        text-align: center;
        text-transform: none;
        touch-action: manipulation;
        user-select: none;
        -webkit-user-select: none;
        vertical-align: middle;
        white-space: nowrap;
        &:focus {
            text-decoration: none;
        }

        &:hover {
            text-decoration: none;
        }

        &:active {
            box-shadow: rgba(0, 0, 0, .125) 0 3px 5px inset;
            outline: 0;
        }

        &:not([disabled]):active {
            box-shadow: #fff 2px 2px 0 0, #000 2px 2px 0 1px;
            transform: translate(2px, 2px);
        }
    }

</style>