<template>
    <div>
        <HomeHeader></HomeHeader>
        <HomeSwiper></HomeSwiper>
        <HomeIcons></HomeIcons>
        <HomeHot></HomeHot>
        <HomeYoulike></HomeYoulike>
    </div>
</template>

<script>
    import HomeHeader from './home/components/Header'
    import HomeSwiper from './home/components/Swiper'
    import HomeIcons from './home/components/Icons'
    import HomeHot from './home/components/Hot'
    import HomeYoulike from './home/components/Youlike'
    export default {
      name: 'Home',
      components:{
        HomeHeader,
        HomeSwiper,
        HomeIcons,
        HomeHot,
        HomeYoulike
      }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
