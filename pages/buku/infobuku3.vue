<template>
    <div class="container-fluid">
      <div class="row">
        <div class="col-lg-12">
          <h2 class="text-center my-4">HELANG DAN PEMBURU</h2>
          <div class="row">
            <div class="col-lg-2">
              <div class="card mb-3">
                <div class="card-body">
                  <img src="~/assets/helang.jpg" class="cover" alt="cover 3">
                </div>  
              </div>
            </div>
            <div class="col-lg-10">
              <div class="card mb-3">
                <h2>TAHUN TERBIT:  24 nov 2020 </h2>
                <h2>PENERBIT: Nur farhan</h2>
                <h2>DESKRIPSI: 
                  Siri Hikayat Teladan ini menghimpun kan pelbagai kisah menarik untuk bacaan santai, tetapi berinformasi sesuai untuk kanak-kanak. Siri ini didatangkan dengan enam tajuk yang berlainan dan perlu dimiliki sebagai koleksi untuk bacaan harian kanak-kanak. Banyak pengajaran dan teladan yang dapat diambil daripada kisah hikayat ini. </h2>
              </div>
            </div> 
            <Nuxt-Link to="/buku"> 
               <button type="submit" class="btn btn-secondary btm-lg rounded-5" style="margin-left: 82%;" >BACK</button>
               </Nuxt-Link> 
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <style scoped>
  .card-body {
    width: 100%;
    height: 20em;
    padding: 0;  
  }
  .cover {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: 0 30;  
  }
  </style>