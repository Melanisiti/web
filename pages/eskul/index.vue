<template>
  <div class="container">
    <h2 class="text-center mb-4">Daftar Ekstrakurikuler</h2>
    <div class="row">
      <div
        class="col" 
        v-for="ekstra in ekstrakurikuler" 
        :key="ekstra.id"
      >
        <div class="card">
          <!-- Gambar Ekstrakurikuler -->
          <img :src="getImagePath(ekstra.gambar)" class="card-img-top" :alt="ekstra.nama" />
          <div class="card-body">
            <h5 class="card-title">{{ ekstra.nama }}</h5>
            <p class="card-text">{{ ekstra.deskripsi }}</p>
            <a :href="ekstra.link" class="btn btn-primary">Lihat Detail</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      ekstrakurikuler: [
        {
          id: 1,
          nama: 'Basket',
          gambar: 'basket.jpeg', 
          deskripsi: 'Ekstrakurikuler olahraga Basket untuk meningkatkan keterampilan bermain bola basket.',
        },
        {
          id: 2,
          nama: 'Futsal',
          gambar: 'futsal.jpeg',
          deskripsi: 'Futsal adalah olahraga bola kecil yang dimainkan secara tim di lapangan mini.',
        },
        {
          id: 3,
          nama: 'Fotografi',
          gambar: 'cj.jpeg',
          deskripsi: 'Mengembangkan kemampuan fotografi dan berkreasi dengan kamera.',
        }
      ]
    };
  },
  methods: {
    // Fungsi untuk mendapatkan path gambar
    getImagePath(image) {
      // Jika gambar adalah URL eksternal, kembalikan langsung
      if (image.startsWith('http')) {
        return image;
      }
      // Gambar lokal di folder assets/img
      return require(`@/assets/img/${image}`);
    }
  }
};
</script>

<style scoped>
.container {
  max-width: 1200px;
  margin: auto;
  padding: 20px;
}

h2 {
  font-size: 2rem;
  color: #424242;
}

.row {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.col {
  flex: 1 0 21%; /* Responsif: 4 kolom di desktop */
  min-width: 250px;
  margin-bottom: 20px;
}

.card {
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  overflow: hidden;
}

.card img {
  max-height: 200px;
  object-fit: cover;
  width: 100%;
}

.card-body {
  padding: 15px;
}

.card-title {
  font-size: 1.25rem;
  color: #333;
  margin-bottom: 10px;
}

.card-text {
  font-size: 1rem;
  color: #555;
  margin-bottom: 15px;
}

.btn {
  font-size: 1rem;
  padding: 8px 20px;
}

/* Responsivitas */
@media (max-width: 768px) {
  .row {
    justify-content: center;
  }

  .col {
    flex: 1 0 45%; /* 2 kolom di layar kecil */
  }
}

@media (max-width: 480px) {
  .col {
    flex: 1 0 100%; /* 1 kolom penuh pada layar ekstra kecil */
  }
}
</style>
