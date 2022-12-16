<template>
  <div class="home-heard-wapper">

    <div class="home-heard-body">

      <div class="home-heard-left">

        <div class="home-heard-left-country-wapper">
          <div class="home-heard-left-country">{{country}}<div class="home-heard-left-country-xia">ˇ</div></div>
          <div class="home-heard-left-countryList">
            <div class="home-heard-left-countryitem" v-for="iten in countryList" :key="iten" @click="choseCountry(iten)">
              {{iten}}
            </div>
          </div>

        </div>


        <div class="home-heard-left-to-ogin">
          <a href="###">
            <span class="to-login">亲，请登录</span>
          </a>
        </div>

        <div class="home-heard-left-iten">
          <a href="###">
            <span class="to-iten">免费注册</span>
          </a>
        </div>

        <div class="home-heard-left-iten">
          <a href="###">
            <span class="to-iten">手机逛淘宝</span>
          </a>
        </div>

        <div class="home-heard-left-iten">
          <a href="###">
            <span class="to-iten">网页无障碍</span>
          </a>
        </div>
      </div>
      <div class="home-heard-right">


        <div class="home-heard-right-wodetaobao">
          <a href="###">
            <span class="wodetaobao">我的淘宝<div class="home-heard-left-country-xia">ˇ</div></span>
          </a>

          <div class="wodetaobao-list">
            <a href="###">
              <div class="wodetaobao-iten">我已买到的宝贝</div>
            </a>
            <a href="###">
              <div class="wodetaobao-iten">我的足迹</div>
            </a>



          </div>

        </div>


        <div class="gouwuche-wapper">

          <a href="###">

              <img class="gouwuche-img" src="@/assets/image/gouwuche.png">

            <div class="name-wapper">

              <span class="gouwuche-name">购物车</span>
            </div>


          </a>


        </div>




        <div class="home-heard-right-wodetaobao">
          <a href="###">
            <span class="wodetaobao">★收藏夹</span>
          </a>

          <div class="wodetaobao-list">
            <a href="###">
              <div class="wodetaobao-iten">收藏的宝贝</div>
            </a>
            <a href="###">
              <div class="wodetaobao-iten">收藏的店铺</div>
            </a>



          </div>

        </div>






        <div class="gouwuche-wapper">

          <a href="###">
            <div class="name-wapper">
              <span class="gouwuche-name">商品分类</span>
            </div>

          </a>

        </div>


        <div class="gouwuche-wapper">

          <a href="###">
            <div class="name-wapper">
              <span class="gouwuche-name">免费开店</span>
            </div>

          </a>

        </div>



        <div class="shuxian">|</div>



        <div class="home-heard-right-wodetaobao">
          <a href="###">
            <span class="wodetaobao">千牛卖家中心<div class="home-heard-left-country-xia">ˇ</div></span>
          </a>

          <div class="wodetaobao-list">
            <a href="###">
              <div class="wodetaobao-iten">开店入住</div>
            </a>
            <a href="###">
              <div class="wodetaobao-iten">我已卖出的宝贝</div>
            </a>
            <a href="###">
              <div class="wodetaobao-iten">出售中的宝贝</div>
            </a>


            <a href="###">
              <div class="wodetaobao-iten">买家服务市场</div>
            </a>


            <a href="###">
              <div class="wodetaobao-iten">买家培训中心</div>
            </a>
            <a href="###">
              <div class="wodetaobao-iten">体检中心</div>
            </a>
            <a href="###">
              <div class="wodetaobao-iten">电商学习中心</div>
            </a>

          </div>

        </div>




        <div class="home-heard-right-wodetaobao">
          <a href="###">
            <span class="wodetaobao">联系客服<div class="home-heard-left-country-xia">ˇ</div></span>
          </a>

          <div class="wodetaobao-list">
            <a href="###">
              <div class="wodetaobao-iten">消费者服务</div>
            </a>
            <a href="###">
              <div class="wodetaobao-iten">卖家客服</div>
            </a>
            <a href="###">
              <div class="wodetaobao-iten">意见反馈</div>
            </a>
            <a href="###">
              <div class="wodetaobao-iten">网页版旺旺</div>
            </a>


          </div>

        </div>




      </div>

    </div>

  </div>
</template>

<script>
export default {
  name: "HomeHeader",

  data(){
    return{
      country: "中国大陆",
      countryList:["全球", "中国大陆", "中国台湾", "中国香港", "中国澳门", "韩国", "马来西亚", "澳大利亚", "新加坡", "新西兰", "加拿大", "日本", "越南", "泰国"],

    }
 },

  methods:{
      choseCountry(countryItem){
        this.country=countryItem;
      }

  }



}
</script>

<style scoped>


.shuxian{
  margin-top: 10px;
}

.home-heard-right>div{
  margin-left: 10px;
}

.gouwuche-wapper:hover .gouwuche-name{
  color: #FF4400;
}

.wodetaobao-iten:hover{
  color: #666666;
}

.gouwuche-img{
  /*height: 12px;*/
  position: relative;
  top: 3px;
  width: 22px;
  /*margin-top: 5px;*/
  /*background-color: #F22E00;*/
}

.gouwuche-name{
  /*inline-size: 36px;*/
}
.name-wapper{
  display: inline-block;
  line-height: 36px;

}



.home-heard-right-wodetaobao{
  padding-left: 5px;
  position: relative;
}
.home-heard-right-wodetaobao:hover{
  background-color: white;
}
.home-heard-right-wodetaobao:hover .wodetaobao-list{
  display: block;
}
.wodetaobao-list{
  left: 0px;
  position: absolute;
  display: none;
  background-color: white;
}

.wodetaobao-iten{
  padding-left: 5px;
  width: 100px;
}
.wodetaobao-iten:hover{
  background-color: #F4F4F4;

}





a{
  text-decoration: none;
}
.home-heard-wapper{
  width: 100%;
  height: 36px;
  background-color: #F5F5F5;
}


.home-heard-body{
  width: 1268.8px;
  min-width: 1268.8px;
  height: 36px;
  margin-left: auto;
  margin-right: auto;
  /*background-color: #b3d4fc;*/
}

.home-heard-left{
  float: left;
  height: 36px;
  display: flex;
  /*background-color: coral;*/
}

.home-heard-right{
  float: right;
  height: 36px;
  display: flex;
  /*background-color: #00aaee;*/
}
.home-heard-left-country-wapper{
  position: relative;
}

.home-heard-left-country{
  width: 67px;
  height: 35px;
  margin: 0 6px;
  font-size: 12px;
  line-height: 34px;
  text-align: center;
  /*background-color: coral;*/

}



.home-heard-left-countryList{
  display: none;
  position: absolute;
  width: 200px;
  height: 200px;
  overflow: auto;
  background-color: white;
}
.home-heard-left-country-wapper:hover {
  background-color: white;
}
.home-heard-left-country-wapper:hover .home-heard-left-countryList{
  display: block;
}

.home-heard-left-countryitem:hover{
  background-color: #F4F4F4;
}
.home-heard-left-countryitem{
  height: 35px;
  line-height: 30px;
  padding-left: 10px;
}
.home-heard-left-country-xia{
  float: right;
  font-size: 16px;
  /*background-color: #666666;*/
  line-height: 20px;
  margin-top: 12px;
}


.home-heard-left-to-ogin{
  margin-left: 10px;
  height: 36px;
}
.to-login{
  line-height: 35px;
  font-size: 12px;
  color: #F22E00;
}

.home-heard-left-iten{
  height: 36px;
  line-height: 35px;
  font-size: 12px;
  margin-left: 10px;

}

.home-heard-left-iten:hover .to-iten{
  color: #F22E00;
}

.home-heard-right-wodetaobao{
  height: 36px;
  line-height: 36px;

}

.wodetaobao:hover {
  color: #FF4400;
}
.wodetaobao{
  padding-right: 5px;
}




</style>