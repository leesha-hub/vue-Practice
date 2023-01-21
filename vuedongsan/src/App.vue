<template>
  
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
    원룸샵
    <h4>{{products.at(0)}}</h4>
    <!-- <h4 class="red" :style="스타일">xx 원룸</h4> -->
    <p>{{ price1 }} 만원</p>
    <button @click="increase">허위매물신고</button><span>신고수 : {{ 신고수 }}</span>
  </div>
  <div>
    <h4>{{products.at(1)}}</h4>
    <p>{{ price2 }} 만원</p>
  </div>
  <div>
    <h4>{{products.at(2)}}</h4>
    <p>{{ price2 }} 만원</p>
  </div>
</template>

<script>

function 어쩌구(){
  console.log("aaaaa");
  console.log("aaaaa");
  console.log("aaaaa");
}

어쩌구();

export default {
  name: 'App',
  data() {
    return {
      price1 : 60,
      price2 : 70,
      //스타일 : 'color:blue',
      products : ['역삼동원룸','천호동원룸','마포구원룸'],
      메뉴들 : ['Home','Shop','About'],
      신고수 : 0,
    }
  },
  methods : {
    increase() {
      this.신고수 += 1;
    }
  },
  components: {
  }
}
</script>

<style>
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
