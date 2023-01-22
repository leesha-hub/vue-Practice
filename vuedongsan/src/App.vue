<template>
  
 <div class="black-bg" v-if="모달창열렸니 == true">
  <div class ="white-bg">
    <h4>상세페이지임</h4>
    <p>상세페이지 내용임</p>
    <button @click="모달창열렸니=false">닫기</button>
  </div>
 </div>

  <div class="menu">
    <a v-for="(a,i) in 메뉴들" :key="a">{{ a }}{{ i }}</a>
    <!-- <a>Products</a> -->
    <!-- <a>About</a> -->
  </div>



    <!-- 
    <img alt="Vue logo" src="./assets/logo.png">
    <div v-for="(b,i) in products" :key="b">
      <h4>{{b}}</h4>
      <h4 class="red" :style="스타일">xx 원룸</h4>
      <p>{{i}} 만원</p>
    </div> 
    -->

  <!-- <input type="text" value="===================================">  -->
  
  <div>
    <img src="./assets/room0.jpg" class="room-img">
    <h4>{{ 원룸들[0].title }}</h4>
    <p>{{ 원룸들[0].price }}원</p>
    <!-- <h4 @click="모달창열렸니 = true">{{products.at(0)}}</h4> -->
    <!-- <h4 class="red" :style="스타일">xx 원룸</h4> -->
    <!-- <p>{{ price1 }} 만원</p> -->
    <button @click="increase(0)">허위매물신고</button><span>신고수 : {{ 신고수[0] }}</span>
  </div>
  <div>
    <img src="./assets/room1.jpg" class="room-img">
    <h4>{{products.at(1)}}</h4>
    <p>{{ price2 }} 만원</p>
    <button @click="increase(1)">허위매물신고</button><span>신고수 : {{ 신고수[1] }}</span>
  </div>
  <div>
    <img src="./assets/room2.jpg" class="room-img">
    <h4>{{products.at(2)}}</h4>
    <p>{{ price2 }} 만원</p>
    <button @click="increase(2)">허위매물신고</button><span>신고수 : {{ 신고수[2] }}</span>
  </div>
</template>

<script>

function 어쩌구(){
  console.log("aaaaa");
  console.log("aaaaa");
  console.log("aaaaa");
}

어쩌구();

import {apple, apple2} from './assets/oneroom.js';

console.log(apple);
console.log(apple2);

import data from './assets/oneroom.js';

console.log(data);

export default {
  name: 'App',
  data() {
    return {
      price1 : 60,
      price2 : 70,
      //스타일 : 'color:blue',
      메뉴들 : ['Home','Shop','About'],
      신고수 : [0,0,0],
      모달창열렸니 : false,
      products : ['역삼동원룸','천호동원룸','마포구원룸'],
      원룸들 : data,
    }
  },
  methods : {
    increase(idx) {
      this.신고수[idx] += 1;
    }
  },
  components: {
  }
}
</script>

<style>
body {
  margin:0
}
div {
  box-sizing: border-box;
}
.black-bg {
  width: 100%; height: 100%;
  background: rgba(0,0,0,0,5);
  position:fixed; padding:20px;
}
.white-bg {
  width:100%; background: white;
  border-radius: 8px;
  padding:20px;
}

.room-img {
  width :100%;
  margin-top: 40px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color : white;
  padding : 10px;
}

</style>
