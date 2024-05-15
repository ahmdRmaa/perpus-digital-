<template>
  <div class="container-fluid">
      <div class="row">
          <div class="col-lg-12">
              <h2 class="text-center my-4">RIWAYAT KUNJUNGAN</h2>
              <div class="my-3">
                  <input v-model="keyword" type="search" class="form-control rounded-5" placeholder="Fiter...">
              </div>
              <div class="my-3 text-muted">menampilkan 1 dari 5</div>
              <table class="table">
                  <thead>
                      <tr>
                          <td>No</td>
                          <td>NAMA</td>
                          <td>KEANGGOTAAN</td>
                          <td>WAKTU</td>
                          <td>KEPERLUAN</td>
                      </tr>
                  </thead>
                  <tbody>
                      <tr v-for="(visitor,i) in visitors" :key="i">
                          <td>{{ i+1 }}.</td>
                          <td>{{ visitor.nama }}</td>
                          <td>{{ visitor.keanggotaan.nama }}</td>
                          <td>{{ visitor.tanggal }}, {{ visitor.waktu }}</td>
                          <td>{{ visitor.keperluan.nama }}</td>
                      </tr>
                  </tbody>
            </table>
          </div>
      </div>
      <nuxt-link to="/">
      <button type="submit" class="btn btn-danger btn-lg rounded-5 px-5">kembali</button></nuxt-link>
  </div>
</template>
<script setup>

const supabase = useSupabaseClient()
const keyword = ref("")
const visitors = ref([])

const getpengunjung = async () => {
  const { data, error } = await supabase
  .from('pengunjung')
  .select('*, keanggotaan(*), keperluan(*)')
  if(data) visitors.value = data 
}

onMounted(() => {
  getpengunjung()
})
</script>

<style scoped>
.btn {
  background-color: #D9D9D9;
}
.form-control{
  background-color: #D9D9D9;
}
</style>