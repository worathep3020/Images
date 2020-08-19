<template>
  <div id="app">
    <div class="row">
    <div class="col-6"><img  src="./assets/cat.jpg"  width="400" height="300">
    <HelloWorld msg="images1"/>
    <counter/>
    </div>
    <div class="col-6"><img  src="./assets/dog2.jpg"  width="400" height="300">
    <HelloWorld msg="images2"/>
    <counter/>
    </div>
    <div class="col-6"><img  src="./assets/dog.jpg"  width="400" height="300">
    <HelloWorld msg="images3"/>
    <counter/>
    </div>
    <div class="col-6"><img  src="./assets/cat3.jpg" width="400" height="300">
    <HelloWorld msg="images4"/>
    <counter/>
    </div>
    </div>
    ชื่อ-นามสกุล <input type="text" v-model="name"/>
    รหัสนศ.<input type="text" v-model="code"/>
    GPA <input type="number" v-model="gpa" step="0.01"/>
    <hr />
    ชื่อ:{{name}} รหัสนศ:{{code}} GPA:{{gpa}}
     
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import counter from './components/counter.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    counter
  },
  data: function(){
   return{
     total: 0,
     name: "",
     code: "",
     gpa: 0.0

   };
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
