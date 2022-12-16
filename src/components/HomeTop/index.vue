<template>
  <div class="home-top-wapper-wapper">

    <div class="home-top-wapper">


      <div class="home-top-left">
        <a href="###">
          <img class="logo" src="@/assets/image/logo.png">
        </a>

      </div>
      <div class="home-top-center">

        <div class="search-wapper">

          <div class="baobei-wapper">


                <div class="baobei" v-for="iten in baobeiList" :key="iten" @click="choseBaobei(iten)">
                  <a href="###"> <span class="baobei-baobei">{{iten}}</span> </a>
                </div>


          </div>


          <div class="shu">|</div>
          <div class="search">

            <input class="search-keyword" v-model="keyword">
          </div>

          <div class="sousuo-wapper">
            <a href="###"><div class="sousuo">搜索</div> </a>
          </div>



        </div>
        <div class="search-list-wapper">

          <div class="search-list" v-for="iten in searchList" :key="iten">
              <a href="###">
                <span class="ssssss">{{iten}}</span>

              </a>
          </div>

        </div>

      </div>
      <div class="home-top-right">

        <img class="erweima" src="@/assets/image/erweima.png" alt="">
        
      </div>





    </div>

  </div>
</template>

<script>
export default {
  name: "HomeTop",
  data(){
    return{


      keyword:"",
      baobei:"宝贝",
      baobeis:["宝贝", "天猫", "店铺"],
      searchList:["新款连衣裙", "四件套", "时尚女鞋", "潮流T恤", "潮流T恤", "潮流T恤", "潮流T恤", "潮流T恤", "潮流T恤", "潮流T恤"]
    }
  },

  computed:{
    baobeiList(){
      var baobeis = this.baobeis;
      baobeis = baobeis.filter(item=>item !== this.baobei);
      baobeis.unshift(this.baobei)
      return baobeis;
    }

  },
  methods:{
    choseBaobei(bbb){
      this.baobei = bbb
    }
  }

}
</script>

<style scoped>

.ssssss:hover{
  color: #FF4400;
}

.erweima{
  width: 74px;
  height: 88px;
  margin-left: 75px;
  margin-top: 20px;
}
.sousuo-wapper{
  width: 70px;
  margin-top: 2px;
  border-radius: 17px;
  height: 35px;
  background-color: #FF7500;
}
.sousuo{
  color: white;
  font-size: 25px;
  /*background-color: #b3d4fc;*/
  text-align: center;
  line-height: 35px;
}
.shu{
  margin-left: 70px;
  font-size: 25px;
  margin-top: 1px;
  color: darkgray;
  margin-right: 5px;
}

.search-keyword{
  height: 36px;
  line-height: 36px;
  font-size: 20px;
  border: none;
  outline: none;
  color: #666666;
  /*background-color: #b3d4fc;*/
  width: 600px;
  margin-top: 1px;

}

.baobei-wapper{
  position: absolute;
  margin-top: 5px;
  margin-left: 11px;
  height: 30px;
  font-size: 20px;
  overflow: clip;

}
.baobei-baobei:hover{
  color: #666666;
  text-decoration: none;
}

.baobei{
  background-color: white;
  width: 60px;
  text-align: center;

}
.baobei-wapper:hover{
  height: 120px;
}
.search-wapper{
  margin-top: 40px;
  height: 40px;
  border-radius: 20px;
  display: flex;
  border: 2px #FF7500 solid;
  background-color: white;
}

.search-list-wapper{
  margin-top: 10px;
}
.search-list{
  display: inline-block;
  margin-right: 15px;
  font-size: 13px;
}

.home-top-wapper-wapper{
  width: 100%;
  height: 135px;
  /*background-color: #FF4400;*/
}

.home-top-wapper{
  width: 1268.8px;
  min-width: 1268.8px;
  margin-left: auto;
  margin-right: auto;
  display: flex;
  height: 135px;
}

.home-top-left{
  width: 250px;
  /*background-color: #666666;*/
}

.home-top-right{
  width: 250px;
  /*background-color: #b3d4fc;*/
}
.home-top-center{
  width: 768.8px;
  /*background-color: yellow;*/
}

.logo{
  width: 150px;
  height: 100px;
  margin-top: 20px;
  margin-left: 50px;
}

a{
  text-decoration: none;
}

</style>