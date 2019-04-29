<template>
    <div class="icons">
        <swiper :options="swiperOption">
            <swiper-slide v-for="(listBlock, key) in page" :key="key">
                <div class="icon" v-for="(item,index) of listBlock" :key="index">
                    <div class="icon-img">
                        <img class="icon-img-content" :src="item.imgUrl">
                    </div>
                    <p class="icon-desc">{{item.title}}</p>
                </div>
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>
<script>
    export default{
        name:'HomeIcons',
        data(){
            return{
                swiperOption: {
                    pagination: '.swiper-pagination'
                },
                iconList:[
                    {    id:'0001',
                        title: "景点门票",
                        imgUrl: "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png"
                    },
                    {   id:'0002',
                        title: "一日游",
                        imgUrl: "http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png"
                    },
                    {   id:'0003',
                        title: "本地玩乐",
                        imgUrl: "http://img1.qunarzz.com/piao/fusion/1803/f5/a963333e1fa802.png"
                    },
                    {   id:'0004',
                        title: "动植物园",
                        imgUrl: "http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png"
                    },
                    {   id:'0005',
                        title: "必游榜单",
                        imgUrl: "http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png"
                    },
                    {   id:'0006',
                        title: "自然风光",
                        imgUrl: "http://img1.qunarzz.com/piao/fusion/1803/96/c70f1e85ae4a4f02.png"
                    },
                    {   id:'0007',
                        title: "海滨海岛",
                        imgUrl: "http://img1.qunarzz.com/piao/fusion/1803/27/dac2bcf9added702.png"
                    },
                    {   id:'0008',
                        title: "踏青赏花",
                        imgUrl: "http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png"
                    },
                    {   id:'0009',
                        title: "城市观光",
                        imgUrl: "http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png"
                    },
                    {   id:'0010',
                        title: "全部玩乐",
                        imgUrl: "http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png"
                    }
                ]
            }
        },
        computed:{
            page(){
                const res=[]
                for(let i in this.iconList){
                    const k = Math.floor(i / 8)
                    if (!res[k]) {
                        res[k] = []
                    }
                    res[k].push(this.iconList[i])
                }
                return res
            }
        }
    }
</script>
<style scoped>
    .swiper-slide{
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -ms-flex-wrap: wrap;
        flex-wrap: wrap;
        width: 100%;
        overflow: hidden;
    }
    .icon{
    overflow :hidden;
    width: 25%;
    padding-top: .1rem;
    text-align: center;
    }
    .item{
    overflow: hidden;
    width: 25%;
    }
    .icon-img-content{
        display: block;
        padding: 0.1rem;
        width: calc(100% - 1rem);
        margin: 0 auto;
        margin-top: 0.05rem;}
   .icon-desc{
    text-align: center;
    line-height: 0.4rem;  }
    .location-wrapper{
    display :flex;
     height :1rem;
     line-height :1rem;}
      .location{
      text-align: center;
       flex: 1;}
</style>