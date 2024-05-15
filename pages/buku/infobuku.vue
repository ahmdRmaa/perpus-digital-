<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-lg-12">
        <h2 class="text-center my-4">SI JUKI SERI KEROYOKAN</h2>
        <div class="row">
          <div class="col-lg-2">
            <div class="card mb-3">
              <div class="card-body">
                <img src="~/assets/juki1.jpg" class="cover" alt="cover 1">

              </div>  
            </div>
          </div>
          <div class="col-lg-10">
            <div class="card mb-3">
              <h2>TAHUN TERBIT:  12 Des 2017 </h2>
              <h2>PENERBIT: Bukune </h2>
              <h2>DESKRIPSI: 
                Si Juki seri Keroyokan adalah kompilasi komik dari Pionicon. Mereka yang menyambut undangan Juki untuk bergabung meliputi Congky, Juleha, Qdjy, Vusya, Hebring, Si Bedil, Raisah, Pavlichenko, Manka dan Zombie Ngehe. Kehadiran para karakter komik dalam seri Keroyokan ini diharap bisa melejitkan popularitas mereka bersama si Juki. </h2>  
            </div>
            <Nuxt-Link to="/buku"> 
               <button type="submit" class="btn btn-secondary btm-lg rounded-5" style="margin-left: 82%;" >BACK</button>
               </Nuxt-Link>
          </div>  
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