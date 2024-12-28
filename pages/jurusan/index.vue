<template>
  <div class="jurusan-page">
    <h1 class="title">Daftar Jurusan di SMKN 4 Tasikmalaya</h1>
    <div class="jurusan-container">
      <!-- Looping through jurusanList array to display each jurusan -->
      <div v-for="jurusan in jurusanList" :key="jurusan.id" class="jurusan-card">
        <!-- Gambar jurusan -->
        <img :src="`${imgpath}/${jurusan.image}`" :alt="jurusan.name" />
        <h2>{{ jurusan.name }}</h2>
        <p>{{ jurusan.description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      imgpath: "~/assets/img",
      jurusanList: [
        {
          id: 1,
          name: 'Pengembangan Perangkat Lunak Dan Gim (PPLG)',
          description: 'Fokus pada pengembangan perangkat lunak, aplikasi, dan pembuatan gim interaktif.',
        },
        {
          id: 2,
          name: 'Teknik Komputer dan Jaringan (TJKT)',
          description: 'Mempelajari jaringan komputer, instalasi, dan perawatan perangkat keras serta keamanan sistem.',
        },
        {
          id: 3,
          name: 'Teknik Bisnis Sepeda Motor (TBSM)',
          description: 'Mempelajari teknik perawatan, perbaikan, dan modifikasi sepeda motor.',
        },
        {
          id: 4,
          name: 'Desain Komunikasi Visual (DKV)',
          description: 'Mempelajari desain grafis, multimedia, animasi, dan pembuatan konten visual untuk berbagai platform.',
        },
        {
          id: 5,
          name: 'Teknik Otomasi Industri',
          description: 'Menguasai teknologi otomatisasi dan sistem pengendalian industri untuk berbagai sektor manufaktur.',
        }
      ]
    };
  }
};
</script>

<style scoped>
.jurusan-page {
  padding: 20px;
  text-align: center;
}

.title {
  font-size: 2.5em;
  margin-bottom: 20px;
  color: #333;
}

.jurusan-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
}

.jurusan-card {
  background: #fff;
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 15px;
  text-align: center;
  width: 300px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.jurusan-card img {
  width: 100%;
  height: 150px;
  object-fit: cover;
  border-radius: 8px 8px 0 0;
}

.jurusan-card h2 {
  font-size: 1.2em;
  margin: 10px 0;
  color: #0078D7;
}

.jurusan-card p {
  font-size: 0.9em;
  color: #555;
}

.jurusan-card:hover {
  transform: translateY(-5px);
}

/* Responsivitas */
@media (max-width: 768px) {
  .jurusan-container {
    justify-content: space-between;
  }

  .jurusan-card {
    width: 45%; /* 2 kolom di layar lebih kecil */
  }
}

@media (max-width: 480px) {
  .jurusan-card {
    width: 100%; /* 1 kolom penuh pada layar lebih kecil */
  }
}
</style>