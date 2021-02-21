<template>
  <div id="app">
  <header class="d-flex flex-column flex-md-row align-items-center p-3 px-md-4 mb-3 bg-body border-bottom shadow-sm">
    <p class="h1 my-0 me-md-auto fw-normal">Aodzi Shop</p>
  </header>
  <main class="container">
    <div class="p-3 mb-2 bg-dark text-white">
    <div class="row row-cols-1 row-cols-md-3 mb-3 text-center">
    <div class="col">
      <div span class="border border-warning">
      <div class="card-header">
        <h4 class="my-0 fw-normal">{{watch1.name}}</h4>
      </div>
      <div class="card-body">
        <img src="https://cy.lnwfile.com/_/cy/_raw/6h/ld/rt.jpg" width=100% height= 100%>
        <ul class="list-unstyled text-small">590 บาท</ul>
        <div id="example-1">
          <button type="button" class="btn btn-warning" v-on:click= "watch1.amount += 1" >ซื้อ</button>
          <p>จำนวน {{ watch1.amount }} เรือน </p>
        </div>
      </div>
    </div>
    </div>
    <div class="col">
      <div span class="border border-warning">
      <div class="card-header">
        <h4 class="my-0 fw-normal">{{watch2.name}}</h4>
      </div>
      <div class="card-body">
        <img src="https://doa.robinson.co.th/media/catalog/product/R/B/RBS33728384.jpg" width=100% height= 100%>
        <ul class="list-unstyled text-small">400 บาท</ul>
        <div id="example-2">
          <button type="button" class="btn btn-warning" v-on:click= "watch2.amount += 1" >ซื้อ</button>
          <p>จำนวน {{ watch2.amount }} เรือน </p>
        </div>
      </div>
    </div>
    </div>
    <div class="col">
      <div span class="border border-warning">
      <div class="card-header">
        <h4 class="my-0 fw-normal">{{watch3.name}}</h4>
      </div>
      <div class="card-body">
        <img src="https://doa.robinson.co.th/media/catalog/product/R/B/RBS30264977.jpg" width=100% height= 100%>
        <ul class="list-unstyled text-small">390 บาท</ul>
        <div id="example-3">
          <button type="button" class="btn btn-warning" v-on:click= "watch3.amount += 1" >ซื้อ</button>
          <p>จำนวน {{ watch3.amount }} เรือน </p>
        </div>
      </div>
    </div>
    </div>
  </div>
    <div class="row row-cols-1 row-cols-md-3 mb-3 text-center">
    <div class="col">
      <div span class="border border-warning">
      <div class="card-header">
        <h4 class="my-0 fw-normal">{{watch4.name}}</h4>
      </div>
      <div class="card-body">
        <img src="http://cn.lnwfile.com/k8ttfm.jpg" width=100% height= 100%>
        <ul class="list-unstyled text-small">259 บาท</ul>
        <div id="example-4">
          <button type="button" class="btn btn-warning" v-on:click= "watch4.amount += 1" >ซื้อ</button>
          <p>จำนวน {{ watch4.amount }} เรือน </p>
        </div>
      </div>
    </div>
    </div>
    <div class="col">
      <div span class="border border-warning">
      <div class="card-header">
        <h4 class="my-0 fw-normal">{{watch5.name}}</h4>
      </div>
      <div class="card-body">
        <img src="http://casio-cmg.com/wp-content/uploads/2015/12/GA-100BW-1A_l.png" width=100% height= 100%>
        <ul class="list-unstyled text-small">450 บาท</ul>
        <div id="example-5">
          <button type="button" class="btn btn-warning" v-on:click= "watch5.amount += 1" >ซื้อ</button>
          <p>จำนวน {{ watch5.amount }} เรือน </p>
        </div>
      </div>
    </div>
    </div>
    <div class="col">
      <div span class="border border-warning">
      <div class="card-header">
        <h4 class="my-0 fw-normal">{{watch6.name}}</h4>
      </div>
      <div class="card-body">
        <img src="https://www.casio-intl.com/product/image/1425303491796/" width=100% height= 100%>
        <ul class="list-unstyled text-small">599 บาท</ul>
        <div id="example-6">
          <button type="button" class="btn btn-warning" v-on:click= "watch6.amount += 1" >ซื้อ</button>
          <p>จำนวน {{ watch6.amount }} เรือน </p>
        </div>
      </div>
    </div>
    </div>
  </div>
  <h4>ราคารวม {{ sum+watch1.amount*watch1.price+watch2.amount*watch2.price+watch3.amount*watch3.price+watch4.amount*watch4.price+watch5.amount*watch5.price+watch6.amount*watch6.price }} บาท</h4>
  <button type="button" class="btn btn-warning" v-on:click="say('สั่งซื้อเสร็จสิ้น')" >สั่งซื้อ</button>
  <input type="button" value=" ยกเลิก " onClick="javascript:location.reload();">
  </div>
  </main>
  </div>
</template> 

<script>
export default {
  name: 'App',
  data(){
    return{
      watch1:{
        name:"G-SHOCK รุ่น GA-400HR 1ADR-BK ",
        price:590,
        amount:0
      },
      watch2:{
        name:"G-SHOCK รุ่น GA-700SE-1A2DR ",
        price:400,
        amount:0
      },
      watch3:{
        name:"G-SHOCK รุ่น GA-100-1A4DR",
        price:390,
        amount:0
      },
      watch4:{
        name:"G-SHOCK รุ่น GA-100-1A1DR ",
        price:259,
        amount:0
      },
      watch5:{
        name:"G-SHOCK CASIO รุ่น GA-100BW-1A ",
        price:450,
        amount:0
      },
      watch6:{
        name:"G-SHOCK CASIO รุ่น GA-100-1A4",
        price:599,
        amount:0
      },
      sum: 0,count:0,say: function (message) {
      alert(message)
    }
    }
  }
}
</script>

