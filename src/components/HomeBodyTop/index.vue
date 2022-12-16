<template>
  <div class="home-body-top-wapper">

    <div class="home-body-top-left">
      <div class="fenlei-wapper">
        <div class="fenlei-top">分类</div>
        <div class="fenlei-top-list" v-for="fenlei in fenleiList" :key="fenlei">
          <a href="###"><span class="fenlei-top-iten">{{fenlei[0]}}</span></a> /
          <a href="###"><span class="fenlei-top-iten">{{fenlei[1]}}</span></a> /
          <a href="###"><span class="fenlei-top-iten">{{fenlei[2]}}</span></a> /
        </div>
      </div>
    </div>


    <div class="home-body-top-right">
        <div class="home-body-top-right-top">

          <div class="xuanze"  v-for=" (xuanze, index) in xuanzeList" :key="xuanze"><a href="###" class="aaaxxx">{{xuanze}}</a><span v-if="index < (xuanzeList.length - 1)" class="shuxian"> | </span></div>

        </div>
        <div class="home-body-top-right-bottom">

          <div class="lunbotu-wapper">

            <div v-for="(lunbotu, index) in lunbotus" :key="lunbotu">
              <a href="###">

                <transition  name="lunbotudonghua">
                  <img :src="lunbotu"
                       v-if="index === lunbotuindex % lunbotus.length"
                       class="lunbotu">
                </transition>

              </a>
            </div>
          </div>

          <div class="denglu-wapper">
            <div class="denglu-img-wapper">
              <img src="@/assets/image/touxiang.jpg" class="touxiang">
            </div>
            <div class="nihao">Hi! 你好</div>
            <div class="zhuce-wapper">

              <a href="###"><div class="xaxaxa a-a"><span class="bbbaaa-a">登录</span></div> </a>
              <a href="###"><div class="xaxaxa b-b"><span class="bbbaaa-b">注册</span></div> </a>
              <a href="###"><div class="xaxaxa c-c"><span class="bbbaaa-c">开店</span></div> </a>

            </div>

            <div class="shoucang-wapper">

              <a href="###">
                <div class="xxx-iten">
                  <div class="tubiao">☆</div>
                  <div>宝贝收藏</div>
                </div>
              </a>
              <a href="###">
                <div class="xxx-iten">
                  <div class="tubiao">⊙</div>
                  <div>买过的店</div>
                </div>
              </a>
              <a href="###">
                <div class="xxx-iten">
                  <div class="tubiao">¤</div>
                  <div>收藏的店</div>
                </div>
              </a>
              <a href="###">
                <div class="xxx-iten">
                  <div class="tubiao">※</div>
                  <div>我的足迹</div>
                </div>
              </a>
            </div>

            <div><a href="###">
              <div class="redian-wapper">

                  <div class="redian">热点</div>
                  <div class="redian-neirong">淘宝平台打击流量造假、黑公关、网络水军公告</div>
              </div>
            </a></div>
          </div>











        </div>


    </div>

  </div>
</template>

<script>
export default {
  name: "HomeBodyTop",
  data(){
    return{

      lunbotuindex:0,
      lunbotus:[
        require("@/assets/image/shop1.png"),
        require("@/assets/image/shop2.jpg"),
        require("@/assets/image/shop3.jpg"),
        require("@/assets/image/shop4.png")],


      xuanzeList:["天猫", "聚划算", "天猫超市", "司法拍卖", "飞猪旅行", "天天特卖", "极有家", "淘宝直播"],
      fenleiList:[
          ["女装", "内衣", "奢侈品"],
          ["女鞋", "男鞋", "香包"],
          ["美妆", "饰品", "洗护"],
          ["手机", "数码", "企业礼品"],
          ["女装", "内衣", "奢侈品"],
          ["女鞋", "男鞋", "香包"],
          ["美妆", "饰品", "洗护"],
          ["手机", "数码", "企业礼品"],
      ]
    }
  },

  created() {

    this.timer = window.setInterval(()=>{
      this.lunbotuindex++;

      // console.log(this.lunbotuindex);

    }, 5000);

  },

  beforeDestroy() {
    window.clearInterval(this.timer);
  }


}
</script>

<style scoped>


.lunbotu-wapper{
  margin-left: 10px;
  margin-top: 10px;
  /*display: none;*/
  width: 564px;
  height: 310px;
  overflow: hidden;
  /*background-color: #FF4400;*/
  position: relative;
  border-radius: 20px;

}


.lunbotu{

  /*position: absolute;*/
  width: 564px;
  height: 310px;
  /*margin-left: 100px;*/
  position: absolute;


}



.lunbotudonghua-enter-active{
  animation: chuxian 1s;

}

.lunbotudonghua-leave-active{
  animation: xiaoshi 1s;

}

@keyframes chuxian {

  from{
    transform: translateX(564px);
  }
  to{
    transform: translateX(0px);


  }
}
@keyframes xiaoshi {

  from{
    transform: translateX(0px);

  }
  to{
    transform: translateX(-564px);


  }
}


.home-body-top-right-bottom{
  display: flex;
}
.tubiao{
  font-size: 25px;
}

.redian-neirong{
  width: 250px;
  white-space: nowrap;
  /* 设置多余文本以省略号的形式出现 */
  text-overflow: ellipsis;
  /* 裁剪多余的内容 */
  overflow: hidden;

}


.redian-wapper{
  font-size: 12px;
  display: flex;
  color: #666666;
  margin-top: 37px;
  margin-left: 30px;
}
.redian{
  text-align: center;
  color: #FF4400;
  background-color: #FFEFEF;
  width: 40px;
  border-radius: 2px;
   margin-right: 5px;
}
.shoucang-wapper{
  display: flex;
  width: 320px;
  margin: 0 auto;
  margin-top: 20px;
}
.xxx-iten{
  font-size: 14px;
  width: 60px;
  margin: 0 10px;
  text-align: center;
}
.xxx-iten:hover{
  color: #FF4400;
}

.zhuce-wapper{
  width: 270px;
  display: flex;
  margin: 10px auto;
}
.xaxaxa{

  width: 80px;
  margin: 0 5px;
  height: 42px;
  border-radius: 21px;
  text-align: center;
  line-height: 42px;
  font-size: 18px;
}

.a-a{
  background-color: #FF5400;
  color: white;
}
.b-b{
  background-color: #FF8A00;
  color: white;

}
.c-c{
  background-color: white;
  outline: #FF4400 1px solid;
  color: #FF4400;
}

/*.bbbaaa-a{*/
/*  width: 80px;*/
/*  color: white;*/
/*  font-size: 18px;*/
/*  align-content: center;*/
/*  line-height: 42px;*/

/*}*/





.nihao{
  width: 100%;
  text-align: center;
  font-size: 20px;
}
.touxiang{
  width: 60px;
  height: 60px;
  border-radius: 30px;
}

.denglu-img-wapper{
  width: 60px;
  height: 60px;
  margin: 20px auto;
}

.denglu-wapper{
  width: 350px;
  margin-left: 10px;
  /*position: absolute;*/
  display: inline-block;
  /*height: 100px;*/
  /*background-color: #FF4400;*/

}






.shuxian{
  color: #E8E3E0;
  font-size: 20px;
}

.home-body-top-right-top{
  /*margin-left: 10px;*/
  display: flex;
  padding-left: 20px;
  margin-right: 40px;
  background-color: #F7F9FA;
  border-radius: 10px;
  margin-bottom: 20px;
}

.xuanze{
  height: 42px;
  line-height: 42px;
  font-size: 18px;
  margin: 0 15px;
}

.xuanze:nth-child(1) .aaaxxx,
.xuanze:nth-child(2) .aaaxxx
{
  color: #FD0036;
}
.xuanze:nth-child(3) .aaaxxx
{
  color: #88C900;
}



.xuanze:hover .aaaxxx {
  color: #FF4400;
}


.fenlei-top-list:hover .fenlei-top-iten,
.fenlei-top-list:hover
{
  color: #FD7400;
}

a{
  text-decoration: none;
}
.fenlei-top-iten:hover {
  color: #FD7400;
  border-bottom: 1px #FD7400 solid;
}

.fenlei-top-list{
  font-size: 15px;
  margin-bottom: 17px;
}

.fenlei-top{
  font-size: 20px;
  /*margin-top: 20px;*/
  /*line-height: 50px;*/
  height: 60px;
  line-height: 60px;
}

.fenlei-wapper{
  width: 250px;
  margin-left: 20px;
  padding-left: 20px;
  background-color: #F7F9FA;
  border-radius: 15px;
  padding-bottom: 5px;
  /*padding-bottom: 5px;*/
}

.home-body-top-wapper{
  display: flex;
  width: 1268.8px;
  margin: 0 auto;
  background-color: white;
  border-radius: 20px;
  padding-top: 24px;


}

.home-body-top-left{
  width: 290px;
  padding-bottom: 20px;
  /*background-color: #F7F9FA;*/
}

.home-body-top-right{
  width: 9748.8px;
  padding-left: 10px;


  /*background-color: #b3d4fc;*/
}

</style>