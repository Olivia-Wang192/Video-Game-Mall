<template>
      <div class="header">
        <div class="headerLogo" @click="home">
            <div class="gta1"><i>GAME</i></div>
            <div class="gta2"><i>GAME</i></div>
        </div>

            <div class="headerMenu">
                <ul class="ulist">
                    <li><div class="textlist"><a class="text">STORE</a>
                        <div class="icon"></div>
                        <div class="downMenu">
                            <a>探索队列</a>
                            <a>新品队列</a>
                            <a>社区推荐</a>
                            <a>交互式推荐</a>
                            <a>热门</a>
                            <a>鉴赏家</a>
                        </div>
                        </div>
                        
                   </li>
                    <li><div class="textlist"><a class="text">COMMEND</a>
                        <div class="icon"></div>
                        <div class="downMenu">
                            <a>热销商品</a>
                            <a>新品商品</a>
                            <a>当前特惠</a>
                            <a>最近更新</a>
                            <a>即将推出</a>
                            <a>开发者</a>
                        </div>
                    </div>
                </li>
                    <li><div class="textlist"><a class="text">TYPE</a>
                        <div class="icon"></div>
                        <div class="downMenu">
                            <a>动作</a>
                            <a>冒险及休闲</a>
                            <a>角色扮演</a>
                            <a>模拟</a>
                            <a>策略</a>
                            <a>体育竞技</a>
                        </div>
                    </div>
                </li>
                    <li><div class="textlist"><a class="text">NEWS</a>
                        <div class="icon"></div>
                        <div class="downMenu">
                            <a>游戏下载</a>
                            <a>新手指引</a>
                            <a>资料库</a>
                            <a>游戏攻略</a>
                            <a>游戏截图</a>
                            <a>问答</a>
                        </div>
                    </div>
                </li>
                </ul>
            </div>
        
        
        <div class="headerReg">
            <a @click="car">CART</a>
        </div>
    </div>
</template>

<script>
export default {
    name:'Nav',
    methods:{
    car(){
       this.$router.push('/car');
    },
    home(){
        this.$router.push('/home');
    },

}

}
</script>

<style>
/* 设置头部样式 */
*{margin:0;padding:0}
li{list-style:none}
img{vertical-align:top;border:none}

.header{
    background-color:black;
    height:120px;
    display: flex;
    
   justify-content: space-between;
    
  }

.headerLogo{
    background-color: black;
    position: relative;
    height:100%;
    flex-basis: 160px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-left: 25PX;
    float: left;
   
  }

  .gta1,.gta2{
    position: absolute;
    color: aqua;
    font-weight: bold;
    font-size: 70px;
    

  }

  .gta2{
    color: #ff0055;
    transform: translate(5px,5px);
    mix-blend-mode: lighten;
    animation: shake 0.6s linear infinite;
  }

  .gta2:hover{
    
    cursor: pointer;
  }

  @keyframes shake{
    33%{
      transform: translate(1px,1px);
    }
    66%{
      transform: translate(-1px,1px);
    }
    100%{
      transform: translate(0,0);
    }
  }

  
  .headerMenu{
    
    height:60px;
    flex-basis: 320px;
    float: left;
    margin-top: 40px;
    
   
    
  }

  ul{
      width: 100%;
      height: 60px;
      display: flex;
      
      margin-top: 10px;
      justify-content: space-between;
  }
  li{
    
     
      height: 100%;
      
  }
  
  .textlist {
    
      
      height: 100%;
      font-size: 25px;
     color: white;
      cursor: pointer;
      

  }

  .text{
    display: block;
    margin-left: 7px;
    margin-right: 7px;
    font-family:fantasy;
    padding: 5px;
  }

  .textlist:hover{
    background-color:#272930;
    color: turquoise;
    
  }
  
  .textlist:hover .icon{
   
   border-color: turquoise transparent transparent transparent;
  }

  .textlist:hover .downMenu{
   display: block; 
  }

  
  .icon{
      width: 0;
      height: 0;
      margin: 0 auto;
      border-width: 6px;
      border-style: solid;
      border-color: white transparent transparent transparent;
  }


  .downMenu{
    display: none;
    position: absolute;
    width: 300px;
    height: 360px;
    float: left;
    top: 100px;
    color: white;
    text-align: center;
    background-color:#272930;
    margin-left: 0px;
    z-index: 999;
  }
  

  .downMenu a{
    display: block;
    width: 100%;
    height: 60px;
    font-size: 15px;
    line-height: 60px;
    

  }

  .downMenu a+a{
   border-top:  1px solid black;

  }

  .downMenu a:hover{
    background-color: #353741;
    color: turquoise;
  }


  .headerReg{
    background-color:black;
    height:55px;
    flex-basis: 315px;
    margin-top: 45px;
    float: right;
    
  }

  .headerReg a{
      display: inline-block;
      height: 40px;
      width: 100px;
      margin-top: 10px;
      margin-right: 20px;
      background-color:black;
      text-align:center;
      letter-spacing: 1px;
      color: white;
      font-weight: bolder;
      line-height: 40px;
      border-radius: 20px;
      border:2px solid white;
  }

  .headerReg a:hover{
      cursor: pointer;
      color: turquoise;
      background-color:white;
  }


</style>