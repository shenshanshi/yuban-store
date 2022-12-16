<template>
  <div class="home-body-bottom-wapper">

    <div class="cainixihuan">

      <div>猜你喜欢</div>
      <button class="gexingtuijian">个性推荐</button>
    </div>


    <div class="shop-wapper">

      <div class="shop-itrn" v-for="(index) in 15" :key="index">
        <a class="shop-a" href="###">
          <div class="shangpin-left">
            <img class="shangpin-img"  :src="shop.url">
          </div>

          <div>

            <div class="shop-biaoti">{{shop.title}}</div>
            <div class="yunsongxian">

              <div><p>运送险费</p></div>

            </div>
            <div class="money">￥{{shop.money}}</div>
          </div>



        </a>


      </div>

    </div>


  </div>

</template>

<script>
export default {
  name: "HomeBodyBottom",
  data(){
    return{
      shop:{
          url: require("@/assets/image/shangpin1.webp"),
          title:"志高小太阳取暖器家用节能烤火器电暖气暖风机速热电暖扇脚烤火炉",
          money:35.6
        }


    }
  }
}
</script>

<style scoped>


.money{
  margin-top: 40px;
  font-size: 20px;
  color: #FF4400;
  margin-left: 20px;
}

.shop-biaoti{
  font-size: 18px;
  line-height: 24px;
  height: 48px;
  overflow: hidden;
  margin-left: 10px;
}

a{
  text-decoration: none;
}
a:hover{
  color: #FF4400;
}

.yunsongxian{
  /*width: 100px;*/
  margin-top: 10px;
  display: inline-block;
  /*width: 100px;*/
  height: 20px;
  /*background-color: #222222;*/
  color: #FF4400;
  margin-left: 10px;
}
.yunsongxian>div{


  width: auto;
  border-radius: 2px;
  outline: 1px solid #FAB596;
  line-height: 20px;
  padding: 0 5px;

}
.shop-biaoti:hover{
  color: #FF4400;
}
.shop-a{
  display: flex;
}
.shangpin-img{
  width: 150px;
  height: 150px;
  border-radius: 8px;
}
.shop-itrn{
  margin-top: 20px;
  padding: 11px;
  width: 369.23px;
  margin-left: 21px;
  display: inline-block;
  height: 150px;
  background-color: #F7F9FA;
  border-radius: 10px;
}
.shop-itrn:hover{

  background-color: white;
  outline: #FF4400 1px solid;
}


.gexingtuijian{
  border: none;
  height: 22px;
  font-size: 15px;
  background-color: #FF8800;
  border-radius: 5px;
  color: white;
  margin-top: 10px;
  margin-left: 5px;
}


.cainixihuan{
  display: flex;
  font-size: 25px;
  margin-left: 20px;

}

.home-body-bottom-wapper{

  width: 1268.8px;
  margin: -20px auto 0 auto;
  background-color: white;
  padding-top: 40px;
  height: 1000px;
}

</style>