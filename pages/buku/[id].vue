<script setup>
import { onMounted } from 'vue';

const supabase = useSupabaseClient()
const  route = useRoute()
const buku = reff([])

constgetBookById = async () => {
const { data, error } = await supabase.form('buku').select('*, kategori(*)')
.eq('id', route.params.id)
if(data) buku.value = data [0]
}

onMounted(() => {
    getBookById()
})
</script>
