<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-lg-12">
        <h2 class="text-center my-4">BUKU</h2>
        <div class="my-3">
          <input type="search" class="form-control  rounded-5" placeholder="Mau Baca Apa Hari Ini?">
        </div>
        <div class="my-3 text-muted">Menampilkan 3 dari 3
        <div class="row">
          <div class="col-lg-2">
            <div class="card mb-3">
        <tbody>
          <tr v-for="(visitor,i) in visitors" :key="i">
            <td>{{ i+1 }}.</td>
            <td>{{ visitor.nama }}</td>
            <td>{{ visitor.keanggotaan.nama }}</td>
            <td>{{ visitor.tanggal }}, {{ visitor.waktu }}</td> 
            <td>{{ visitor.keperluan.nama }}</td>
          </tr>
        </tbody>
              <nuxt-link to="/buku/infobuku">
              <div class="card-body">
                <img src="~/assets/juki1.jpg" class="cover" alt="cover 1">
              </div>
            </nuxt-link>
            </div>
          </div>  
          <div class="col-lg-2">
            <div class="card mb-3">
              <nuxt-link to="/buku/infobuku2">
              <div class="card-body">
                <img src="~/assets/kancil.jpg" class="cover" alt="cover 2">
              </div>  
              </nuxt-link>
            </div>
          </div>
          <div class="col-lg-2">
            <div class="card mb-3">
              <nuxt-link to="/buku/infobuku3">
              <div class="card-body">
                <img src="~/assets/helang.jpg" class="cover" alt="cover 3">
              </div>  
              </nuxt-link>
            </div>
            <Nuxt-Link to="/"> 
               <button type="submit" class="btn btn-secondary btm-lg rounded-5" style="margin-left: 82%;" >BACK</button>
               </Nuxt-Link>
          </div>
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

<script setup>
const supabase = useSupabaseClient()

const books = ref([])

const getBooks = async () => {
  const { data, error } = await supabase.form('buku').select('*, kategori(*)')
  if(data) books.value = data
}

onMounted(() => {
  getBooks()
})
</script>