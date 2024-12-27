<template>
  <div class="jurusan-page">
    <h1 class="title">Daftar Jurusan di SMKN 4 Tasikmalaya</h1>
    <div class="jurusan-container">
      <div v-for="jurusan in jurusanList" :key="jurusan.id" class="jurusan-card">
        <img :src="jurusan.image" :alt="jurusan.name" />
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
      jurusanList: [
        {
          id: 1,
          name: 'Pengembangan Perangkat Lunak dan Gim',
          description: 'Fokus pada pengembangan aplikasi, perangkat lunak, dan pembuatan gim interaktif.',
          image: require('~/assets/img/pplg.png')
        },
        {
          id: 2,
          name: 'Teknik Komputer dan Jaringan',
          description: 'Mempelajari jaringan komputer, keamanan sistem, dan administrasi server.',
          image: require('~/assets/img/tkj.png')
        },
        {
          id: 3,
          name: 'Desain Komunikasi Visual',
          description: 'Mengembangkan kreativitas di bidang desain grafis, multimedia, dan animasi.',
          image: require('~/assets/img/dkv.png')
        },
        {
          id: 4,
          name: 'Teknik Sepeda Motor',
          description: 'Belajar tentang perawatan, perbaikan, dan modifikasi sepeda motor.',
          image: require('~/assets/img/tsm.png')
        },
        {
          id: 5,
          name: 'Teknik Otomasi Industri',
          description: 'Menguasai teknologi otomasi dan pengendalian industri modern.',
          image: require('~/assets/img/toi.png')
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
  font-size: 2em;
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
</style>
