<template>
<div id="app">
  
    <!-- <h class="h3 my-0 me-md-auto fw-normal"><b>Shop-Me.</b></h>
 <br /> <br />
  <main class="container">
  <h4>ราคารวม {{ sum+product1.amount*product1.price+product2.amount*product2.price+product3.amount*product3.price+product4.amount*product4.price+product5.amount*product5.price+product6.amount*product6.price }} บาท</h4>
    <div class="row row-cols-1 row-cols-md-3 mb-3 text-center">
    <div class="col">
      <div class="card mb-4 shadow-sm">
      <div class="card-header">
        <h4 class="my-0 fw-normal">{{product1.name}}</h4>
      </div>
      </div>
    </div>
     
      -->
     
    
    <b-card img-src="https://placekitten.com/300/300" img-alt="Card image" img-left class="mb-3">
      <b-card-text>
        Some quick example text to build on the card and make up the bulk of the card's content.
      </b-card-text>
       <b-button  variant="primary"  style="width: 200px; height: 50px"  v-on:click= "product1.amount += 1" >+</b-button>
          <p>จำนวน {{ product1.amount }} ถุง </p>
         <b-button  variant="primary"  style="width: 200px; height: 50px" v-on:click= "product1.amount -= 1" >-</b-button>
    </b-card>

    <b-card img-src="https://placekitten.com/300/300" img-alt="Card image" img-right>
      <b-card-text>
        Some quick example text to build on the card and make up the bulk of the card's content.
      </b-card-text>
    </b-card>
  

     
     
      <!-- <div class="card-body">
        <img src="https://th-live-01.slatic.net/p/dab02a3da4358760cf8d30597ce93139.jpg"
        img height = "250">
        <ul class="list-unstyled text-small">ราคา 20 บาท</ul>
        <div id="example-1">
         
        </div>
      </div>
    </div>
    
    <div class="col">
      <div class="card mb-4 shadow-sm">
      <div class="card-header">
        <h4 class="my-0 fw-normal">{{product2.name}}</h4>
      </div>
      <div class="card-body">
        <img src="https://lh3.googleusercontent.com/proxy/VqX0-Lkcm7lvT8ZfD1RJQGhBsKrkyhy3arqLVBcuAguuevbBGjqftMI_VUAuhGu1wqqQJF3OpGP-pzqgmZrQlAV3ZFCPrFOdem2K5mTuzjINs9Gu"
        img height = "250">
        <ul class="list-unstyled text-small">ราคา 15 บาท</ul>
        <div id="example-2">
          <button type="button" class="w-100 btn btn-lg btn-outline-success" v-on:click= "product2.amount += 1" >+</button>
          <p>จำนวน {{ product2.amount }} ขวด </p>
           <button type="button" class="w-100 btn btn-lg btn-outline-danger" v-on:click= "product2.amount -= 1" >-</button>
        </div>
      </div>
    </div>
    </div>
    <div class="col">
      <div class="card mb-4 shadow-sm">
      <div class="card-header">
        <h4 class="my-0 fw-normal">{{product3.name}}</h4>
      </div>
      <div class="card-body">
        <img src="https://secure.ap-tescoassets.com/assets/TH/968/8850250010968/ShotType1_540x540.jpg"
        img height = "250">
        <ul class="list-unstyled text-small">ราคา 15 บาท</ul>
        <div id="example-3">
          <button type="button" class="w-100 btn btn-lg btn-outline-success" v-on:click= "product3.amount += 1" >+</button>
          <p>จำนวน {{ product3.amount }} ชิ้น </p>
           <button type="button" class="w-100 btn btn-lg btn-outline-danger" v-on:click= "product3.amount -= 1" >-</button>
        </div>
      </div>
    </div>
    </div>
  </div>
    <div class="row row-cols-1 row-cols-md-3 mb-3 text-center">
    <div class="col">
      <div class="card mb-4 shadow-sm">
      <div class="card-header">
        <h4 class="my-0 fw-normal">{{product4.name}}</h4>
      </div>
      <div class="card-body">
        <img src="https://secure.ap-tescoassets.com/assets/TH/576/8850144206576/ShotType1_540x540.jpg"
        img height = "250">
        <ul class="list-unstyled text-small">ราคา 10 บาท</ul>
        <div id="example-4">
          <button type="button" class="w-100 btn btn-lg btn-outline-success" v-on:click= "product4.amount += 1" >+</button>
          <p>จำนวน {{ product4.amount }} กล่อง </p>
           <button type="button" class="w-100 btn btn-lg btn-outline-danger" v-on:click= "product4.amount -= 1" >-</button>
        </div>
      </div>
    </div>
    </div>
    <div class="col">
      <div class="card mb-4 shadow-sm">
      <div class="card-header">
        <h4 class="my-0 fw-normal">{{product5.name}}</h4>
      </div>
      <div class="card-body">
        <img src="https://cf.shopee.co.th/file/dd09405633c746f542c9f7e28f9dceb1"
        img height = "250">
        <ul class="list-unstyled text-small">ราคา 45 บาท</ul>
        <div id="example-5">
          <button type="button" class="w-100 btn btn-lg btn-outline-success" v-on:click= "product5.amount += 1" >+</button>
          <p>จำนวน {{ product5.amount }} ขวด </p>
          
        </div>
      </div>
    </div>
    </div>
    <div class="col">
      <div class="card mb-4 shadow-sm">
      <div class="card-header">
        <h4 class="my-0 fw-normal">{{product6.name}}</h4>
      </div>
      <div class="card-body">
        <img src="https://static.bigc.co.th/media/catalog/product/8/8/8850069010036.jpg"
        img height = "250">
        <ul class="list-unstyled text-small">ราคา 20 บาท</ul>
        <div id="example-6">
          <button type="button" class="w-100 btn btn-lg btn-outline-success" v-on:click= "product6.amount += 1" >+</button>
          <p>จำนวน {{ product6.amount }} ถุง </p>
           <button type="button" class="w-100 btn btn-lg btn-outline-danger" v-on:click= "product6.amount -= 1" >-</button>
        </div>
      </div>
    </div>
    </div>
  </div>
  
  <b-button variant="w-50 btn btn-lg btn-outline-success" v-on:click="say('ขอบคุณที่ใช้บริการของร้าน Shop-Me.')" >สั่งซื้อ</b-button>
  &nbsp; &nbsp;
  <b-button variant="w-50 btn btn-lg btn-outline-primary"  value="Reset" onClick="javascript:location.reload();">Reset</b-button>
   -->
  <!-- </main> -->
</div>

</template> 

<script>
export default {
  name: 'App',
  data(){
    return{
      product1:{
        name:"น้ำตาล",
        price:20,
        amount:0
      },
      product2:{
        name:"น้ำปลา",
        price:15,
        amount:0
      },
      product3:{
        name:"รสดี",
        price:15,
        amount:0
      },
      product4:{
        name:"คะนอร์",
        price:10,
        amount:0
      },
      product5:{
        name:"น้ำมันพืช",
        price:45,
        amount:0
      },
      product6:{
        name:"เกลือ",
        price:20,
        amount:0
      },
      sum: 0,count:0,say: function (message) {
      alert(message)
    }
    }
  }
}
</script>
