<template>
  <div class="home-wapper">

    <HomeHeader></HomeHeader>
    <HomeTop></HomeTop>
    <HomeBody></HomeBody>
  </div>
</template>

<script>

import HomeHeader from "@/components/HomeHeader";
import HomeTop from "@/components/HomeTop";
import HomeBody from "@/components/HomeBody";
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Home",
  components:{HomeHeader, HomeTop, HomeBody}
}
</script>

<style scoped>
.home-wapper{
  min-width: 1268.8px;
}
</style>