<template>
<div>
  
    <button @click="upFunction()" class="btn btn-dark btn-outline-primary "><i class="fa fa-thumbs-up"></i>like</button>
    <button @click="downFunction()" class="btn btn-dark btn btn-secondary "><i class="fa fa-thumbs-down"></i>Dislike</button>
    <button @click="lovecount()" class="btn btn-dark btn-outline-danger "><i class="fa fa-heart"></i>Love</button>
    <button @click="reset()" class="btn btn-dark btn-outline-success "><i class="fa fa-trash"></i>Reset</button>
    <p v-bind:style="{ fontSize: fsize + 'px' }">{{ counter }}</p>
  
  </div>
 
</template>

<script>
export default {
  data: function () {
    return {
      counter: 0,
      fsize: 50,
    };
  },

  props: {
    lable: String,
  },

  methods: {
    upFunction: function () {
      this.counter += 1;
      console.log(this.counter);

    },

    downFunction: function () {
      this.counter -= 10;

      //console.log(this.fsize);
      console.log(this.counter);
    },
    lovecount: function (){
      this.counter += 5;
      console.log(this.counter);

    },
    reset: function () {
      this.counter = 0;
      console.log(this.counter);

    },
  },
};
</script>


<style>
</style>
