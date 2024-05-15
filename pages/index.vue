<template>
  <div class="container-fluid">
    <div class="row my-5">
      <div class="col-lg-6">
        <nuxt-link to="/pengunjung/tambah">
          <div class="card bg-pengunjung rounded-5">
            <div class="card-body">
              <h2>Pengunjung</h2>
            </div>
          </div>
        </nuxt-link>
      </div>

       <div class="col-lg-6">
         <nuxt-link to="/buku">
           <div class="card bg-buku rounded-5">
             <div class="card-body">
               <h2>Cari Buku</h2> 
             </div>
           </div>
         </nuxt-link>
       </div>
     </div>
   </div> 
   <h2 style="margin: 30px;"><strong>STATISTIK</strong></h2>
   <div class="container-fluid">
    <div class="row justify-content-evenly rounded-3">
      <div class="col-5">
        <nuxt-link to="/pengunjung">
          <div class="card bg-light rounded-5">
            <div class="card-body">
              <div class="card1">
                <div class="romo">
                  <h2>3 Pengunjung</h2>
                </div>

              </div>
            </div>
          </div>
        </nuxt-link>
      </div>
      
      
      <div class="col-5">
            <div class="romo2">
              <h2>102 Buku</h2>
              
            </div> 
          </div>
        </div>
      </div>

   
</template>

<style scoped>
.v2 {
    height: 3px;
    width: 98%;
    margin-left: 30px;
    border-left: 3px solid black;
    background-color: black;
}
.v1 {
    margin-top: 40px;
    margin-left: 30px;
    border-left: 3px solid black;
    height: 400px;
}
.card {
  height: 250px;
  box-shadow: 1px 1px 1px #424242;
}
.card.bg-pengunjung {
  background-image: url('~/assets/bgkunjungan.jpeg');
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
}
.card.bg-buku {
  background-image: url('~/assets/bgcaribuku.jpg');
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;  
}
.card.bg-light {
  background-color: darkkhaki;
}
.romo {
    height: 200px;
    box-shadow: 1px 1px 10px;
    border-radius: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #F0F1A8;
}
.romo2 {
    height: 200px;
    box-shadow: 1px 1px 10px;
    border-radius: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #CCF29A;
}
  
</style>