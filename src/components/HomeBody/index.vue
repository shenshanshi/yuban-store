<template>
  <div class="home-body-wapper">
    <HomeBodyTop></HomeBodyTop>
    <HomeBodyBottom></HomeBodyBottom>

  </div>
</template>

<script>
import HomeBodyTop from "@/components/HomeBodyTop";
import HomeBodyBottom from "@/components/HomeBodyBottom";
export default {
  name: "HomeBody",
  components:{HomeBodyTop, HomeBodyBottom}
}
</script>

<style scoped>

.home-body-wapper{
  width: 100%;
  /*height: 1000px;*/
  /*background-color: darkgray;*/
}

</style>