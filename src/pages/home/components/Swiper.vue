<template>
    <div>
        <swiper :options="swiperOption">
            <!-- slides -->
            <swiper-slide v-for="itme in swiperList" :key="id">
                <img class="swiper-img" :src="itme.imgUrl">
            </swiper-slide>
            <!-- Optional controls -->
            <div class="swiper-pagination" ></div>
        </swiper>
    </div>
</template>
<script>
    export default{
        name:'HomeSwiper',
        data (){
            return{
                swiperOption: {
                    pagination: '.swiper-pagination'
                },
                swiperList:[
                    {
                    id:'0001',
                    imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/c807f8e462d269397489ef90b16f61b7.jpg_750x200_aaf543ba.jpg'
                     },
                    {
                        id:'0002',
                        imgUrl:'http://img1.qunarzz.com/piao/fusion/1805/fe/ca8ed7adc3ff9f02.jpg_750x200_49735140.jpg'
                    },
                    {
                        id:'0003',
                        imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/a9658b2ee2c2c6de227c9710a8b04d48.jpg_750x200_f38fba28.jpg'
                    },
                    {
                        id:'0004',
                        imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/87a224d0349d94a11e97f31aa1aba4f5.jpg_750x200_1f78af87.jpg'
                    }

                ]
            }
        }
    }
</script>
<style  lang="less">
    .swiper-pagination-bullet-active{
        background-color: #fff !important;
    }
    .swiper-img{
        width: 100%;
    }
</style>